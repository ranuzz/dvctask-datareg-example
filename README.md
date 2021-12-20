## Data Registry Example : DVC

Created this readme and initialised both git and dvc

## Data

created two csv files in local storage to act as data source

## remote

Created S3 bucket 
https://s3.console.aws.amazon.com/s3/buckets/dvctask?region=us-west-1&tab=objects

s3://dvctask/sample/
https://dvctask.s3.us-west-1.amazonaws.com/sample/

```sh
dvc remote add -d myremote s3://dvctask/sample/
```

adds entry in .dvc/config

```txt
[core]
    remote = myremote
['remote "myremote"']
    url = s3://dvctask/sample/
```

no need to add creds it will come later with push

google drive

dvc remote add -d myremote gdrive://1zSABJlHwuYvTCUvHL1wQQs4w-Mi3iMdI/xxx


## data add

copy the data to this directory

mkdir data
cp * data/

dvc add data/

git add .gitignore data.dvc

git commit 

dvc push