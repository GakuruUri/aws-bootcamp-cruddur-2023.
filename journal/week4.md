# Week 4 — Postgres and RDS

## Creating DB Instance

![creating DB instance](https://user-images.githubusercontent.com/27725033/228920229-28607a20-ef04-4864-a5a9-161f93da2a50.png)

![Creating DB on AWS UI](https://user-images.githubusercontent.com/27725033/228920292-e4f950f4-5631-4ea4-9467-034083d678e9.png)

## Testing PostgreSQL

![Postgres Working](https://user-images.githubusercontent.com/27725033/228920394-e228ebb9-3274-4f30-bd16-e9a50968c838.png)

![Creating an extension](https://user-images.githubusercontent.com/27725033/228920462-1da58b0c-7be5-4379-8300-4e48954ae2fd.png)

## Connecting to Cruddur DB

![Connected to crudder db](https://user-images.githubusercontent.com/27725033/228920577-bc1f7bcc-6202-475e-b78a-74f4c34b461d.png)

![SetUp password for crudder cli](https://user-images.githubusercontent.com/27725033/228920689-598505c4-29b0-4601-93f4-1b8f0c8a83c5.png)

![Change Mode 400](https://user-images.githubusercontent.com/27725033/228920772-23febbca-b0dc-4486-a9be-413d54684b54.png)

![SED DB Drop](https://user-images.githubusercontent.com/27725033/228920853-ebf79913-a958-4132-88c1-2d602355dd84.png)

![Db Create SED](https://user-images.githubusercontent.com/27725033/228920891-0bfa7b35-853a-4f2b-aa52-201098b38fd6.png)

![Schema absolute path](https://user-images.githubusercontent.com/27725033/228920925-e7e42743-6bb6-450e-818d-f5ac793d8379.png)

![Schema loading](https://user-images.githubusercontent.com/27725033/228920956-3cfcd81c-521b-4a2c-8b15-2329c5268ef1.png)


## DB Instance create

aws rds create-db-instance \
  --db-instance-identifier cruddur-db-instance \
  --db-instance-class db.t3.micro \
  --engine postgres \
  --engine-version  14.6 \
  --master-username root \
  --master-user-password ******* \
  --allocated-storage 20 \
  --availability-zone us-east-1a \
  --backup-retention-period 0 \
  --port 5432 \
  --no-multi-az \
  --db-name cruddur \
  --storage-type gp2 \
  --publicly-accessible \
  --storage-encrypted \
  --enable-performance-insights \
  --performance-insights-retention-period 7 \
  --no-deletion-protecti


## ARNs for use in lambda creation

https://github.com/jetbridge/psycopg2-lambda-layer

functions:
  hello:
    handler: handler.hello
    layers:
      # py 3.6:
      - arn:aws:lambda:us-east-1:898466741470:layer:psycopg2-py36:3
      - arn:aws:lambda:us-east-2:898466741470:layer:psycopg2-py36:1
      - arn:aws:lambda:us-west-2:898466741470:layer:psycopg2-py36:1
      - arn:aws:lambda:eu-central-1:898466741470:layer:psycopg2-py36:2
      - arn:aws:lambda:sa-east-1:898466741470:layer:psycopg2-py36:1
      # py 3.7:
      - arn:aws:lambda:eu-central-1:898466741470:layer:psycopg2-py37:6
      - arn:aws:lambda:ap-southeast-1:898466741470:layer:psycopg2-py37:1
      - arn:aws:lambda:us-east-1:898466741470:layer:psycopg2-py37:3
      - arn:aws:lambda:us-east-2:898466741470:layer:psycopg2-py37:1
      - arn:aws:lambda:us-west-2:898466741470:layer:psycopg2-py37:7
      - arn:aws:lambda:eu-west-1:898466741470:layer:psycopg2-py37:1
      - arn:aws:lambda:eu-west-2:898466741470:layer:psycopg2-py37:1
      - arn:aws:lambda:eu-west-3:898466741470:layer:psycopg2-py37:1
      - arn:aws:lambda:sa-east-1:898466741470:layer:psycopg2-py37:1
      - arn:aws:lambda:ap-southeast-1:898466741470:layer:psycopg2-py37:5
      - arn:aws:lambda:ap-southeast-2:898466741470:layer:psycopg2-py37:1
      - arn:aws:lambda:ca-central-1:898466741470:layer:psycopg2-py37:1
      - arn:aws:lambda:ap-south-1:898466741470:layer:psycopg2-py37:1
      # py 3.8:
      - arn:aws:lambda:ca-central-1:898466741470:layer:psycopg2-py38:1
      - arn:aws:lambda:us-east-1:898466741470:layer:psycopg2-py38:2
      - arn:aws:lambda:us-east-2:898466741470:layer:psycopg2-py38:1
      - arn:aws:lambda:us-west-1:898466741470:layer:psycopg2-py38:1
      - arn:aws:lambda:us-west-2:898466741470:layer:psycopg2-py38:1
      - arn:aws:lambda:eu-west-1:898466741470:layer:psycopg2-py38:1
      - arn:aws:lambda:eu-west-2:898466741470:layer:psycopg2-py38:1
      - arn:aws:lambda:eu-west-3:898466741470:layer:psycopg2-py38:1
      - arn:aws:lambda:eu-central-1:898466741470:layer:psycopg2-py38:1
      - arn:aws:lambda:eu-south-1:898466741470:layer:psycopg2-py38:1
      - arn:aws:lambda:ap-northeast-1:898466741470:layer:psycopg2-py38:1
      - arn:aws:lambda:ap-southeast-1:898466741470:layer:psycopg2-py38:1
      - arn:aws:lambda:ap-southeast-2:898466741470:layer:psycop


![ARN for us-east1](https://user-images.githubusercontent.com/27725033/228923709-5921dbcd-a7bd-448d-aa3a-0a25ca30c4a9.png)






![Schema loading](https://user-images.githubusercontent.com/27725033/228921666-73f93c4b-9907-427e-bc42-2cfb1c852b5d.png)

![Color working](https://user-images.githubusercontent.com/27725033/228921696-4b65579b-2f99-44bb-8ef1-c991a9aabe13.png)

![Seed Data](https://user-images.githubusercontent.com/27725033/228921719-c16fd0e2-c093-45f3-97b9-0eeb974e10ff.png)

## DB Errors

![DB Errors connecting](https://user-images.githubusercontent.com/27725033/228921812-d1ca213a-8fbe-4e21-b2b6-ac5a1d5f3cd2.png)

## Solution

![Researching for solutions](https://user-images.githubusercontent.com/27725033/228921934-d1728eb3-90ca-4b6a-912d-db0a6e9f3a77.png)


![Tables View](https://user-images.githubusercontent.com/27725033/228922001-038a4627-4158-488b-8bd6-95b5e929a0d8.png)

![DB Setup](https://user-images.githubusercontent.com/27725033/228922025-3d94371e-cfa8-47da-bdda-b74fe53aac1f.png)


![Connection Pooling](https://user-images.githubusercontent.com/27725033/228922063-da3a855a-f7e3-460f-8828-e50f2b04c2fe.png)

![Firdt Querry data](https://user-images.githubusercontent.com/27725033/228922086-43c0070d-ae30-490b-8887-bd3df1302ee6.png)


## Getting Gitpod IP

![Get GITPOD IP](https://user-images.githubusercontent.com/27725033/228935264-624650fd-99d5-42f4-8227-c11a9ec51cd5.png)




![Finally connected to RDS](https://user-images.githubusercontent.com/27725033/228923166-763df0bc-6601-4b38-814c-9d4e13e7fa68.png)


## Security Groups

![SG set successfully](https://user-images.githubusercontent.com/27725033/228923213-fb335517-7278-4c55-b987-b5938e8da143.png)

![Modified SG rule from GITPOD Script](https://user-images.githubusercontent.com/27725033/228923562-37878b6c-1632-4589-8276-63b1c193d44b.png)


![SG rule worked on startup](https://user-images.githubusercontent.com/27725033/228923600-98eeecc4-7924-4f99-931a-faa58a9a996f.png)


![Connected to prd DB](https://user-images.githubusercontent.com/27725033/228923626-17e6a1fd-1ca1-40f2-a167-e083511764aa.png)


## Confirmation Error

![Post confirmation Error](https://user-images.githubusercontent.com/27725033/228923764-aa8d804c-a28f-416d-bb1e-4091c2980db9.png)


https://stackoverflow.com/questions/41177965/aws-lambdathe-provided-execution-role-does-not-have-permissions-to-call-describ

![Cognito SignUp Errors](https://user-images.githubusercontent.com/27725033/228923903-a63177cf-2e1f-4fb7-a647-22ee009cb2ca.png)


![Cognito SignUp Errors](https://user-images.githubusercontent.com/27725033/228923940-bbff9cc0-7eb6-4145-babf-4ac3618cbf91.png)


## Created a user

![posting worked!!!!](https://user-images.githubusercontent.com/27725033/228924261-7aae6188-606c-40cd-8f90-5d27106ad9f0.png)

![DB created users](https://user-images.githubusercontent.com/27725033/228924371-3cae39d3-a62b-4422-b2d3-c12b583e6203.png)







