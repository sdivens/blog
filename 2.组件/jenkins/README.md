# jenkins 
## 项目持续集成调度器

```bash
pipeline {
    agent any
    parameters {
        string(name: 'JOB_DATE', defaultValue: '', description: '任务日期yyyyMMdd')
    }
    stages {
        stage('Parallel Stage') {
            failFast false
            parallel {
                stage('Branch A') {
                    agent {
                        label "Marmot-dnode02"
                    }
                    steps {
                        aaa= {build job: 'Marmot-1-m2h-ods-jianlc-interest', parameters: [string(name: 'JOB_DATE', value: "${JOB_DATE}")],wait:true}
                        echo aaa.number
                    }
                }
                stage('Branch B') {
                    agent {
                        label "Marmot-dnode02"
                    }
                    steps {
                        bbb={build job: 'Marmot-1-m2h-ods-product', parameters: [string(name: 'JOB_DATE',value: "${JOB_DATE}")],wait:true}
                        echo bbb.result
                    }
                }
            }
        }
    }
}
```