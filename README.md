# BigData_AWS_EMR_MRJob_DIO

Este é um projeto de processamento distribuído de dados utilizando Python, MRJob e AWS EMR, que faz parte do Curso __*Criando seu Ecossistema de Big Data na Nuvem*__ do Bootcamp Cloud Data Engineer, promovido pela [Digital Innovation One](https://web.digitalinnovation.one/home).

---

## Instruções

* Acessar S3: https://s3.console.aws.amazon.com/s3/ 
  * Criar estrutura de data lake : _dio-datalake_
  * Criar estrutura de pastas:
    * _data_
    * _output_
    * _temp_
* Acessar EMR: https://console.aws.amazon.com/elasticmapreduce/
    * O cluster será criado pelo MrJob e não pelo console
    * Infraestrutura como código 
* Criar chave SSH
    * Acessar  Console do EC2: https://console.aws.amazon.com/ec2/ -> Key Pairs -> Create Key Pair	
    * Download .pem file
* Obter Id e chave secreta AWS para configurar MrJob
   * Profile
   * My Security Credentials: https://console.aws.amazon.com/iam/home?region={region}#/security_credentials
   * Access Keys - Create new access key
   * Fazer download - única chance de visualizar
* Ambiente linux
   * Criar ambiente virtual python: ```virtualenv --python=python3.6 venv_emr```
* Criar algoritmo de análise de palavras
   * ```wordcount-test.py```
   * map-reduce-count
   * Instalar boto3: ```pip install boto3```
   * Instalar mrjob: ```pip install mrjob```
* Acessar S3
   * Upload de arquivo para o bucket
* Ambiente virtual python: ```source venv_teste/bin/activate```
  * _nano ~/.mrjob.conf_
  * ```python3 wordcount-test.py -r emr s3://{your_s3_bucket_name}/data/SherlockHolmes.txt --output-dir=s3://{your_s3_bucket_name}/output/logs1 --cloud-tmp-dir=s3://{your_s3_bucket_name}/temp/```

---

![Arquitetura_EMR_S3_MRJob](https://miro.medium.com/max/770/1*uPr46z555fiJfHeaz8gh3g.png)
