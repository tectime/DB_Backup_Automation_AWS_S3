# PGBACKUP TOOL

Remote or local backup automation script with remote upload option for AWS S3 repositories.

### Features

- CLI for backing up remote PostgreSQL databases locally or to AWS S3.


How to install
-------------------------

### Python
- Support standard: all versions of Linux with Python 3.6 or higher

### Install pip

`$ sudo yum install epel-release`

`$ sudo yum install python36-pip`

### How to Install AWS CLI

https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html

### Installing pgbackup ool

Download the file:

`$ curl https://github.com/tectime/DB_Backup_Automation_AWS_S3/raw/main/dist/pgbackup-0.1.0-py36-none-any.whl -o ./pgbackup-0.1.0-py36-none-any.whl`

Install de pgbackup package using the pip command"

`$ pip install dist/pgbackup-0.1.0-py36-none-any.whl`

How to install
-------------------------

Pass in a full database URL, the storage driver, and destination.

#### S3 Example w/ bucket name:

$ pgbackup --driver s3 Your_S3_Bucket_name postgres://database_name:1234@server_ip:80/sample

Example
`$ pgbackup --driver s3 robsonmessias1 postgres://db_rob_test:1234@3.250.212.103:80/sample`

#### Local Example w/ local path:

` $ pgbackup --driver local ./local-dump.sql postgres://db_rob_test:1234@3.250.12.200:80/sample`

Preparing for Development
-------------------------

  1. Ensure ``pip`` and ``pipenv`` are installed
  2. Clone repository: 
  ``git clone git@https://github.com/tectime/DB_Backup_Automation_AWS_S3``
  3. ``cd`` into repository
  4. Fetch development dependencies ``make install``
  5. Activate virtualenv: ``pipenv shell``

Usage
-----

Pass in a full database URL, the storage driver, and destination.

#### S3 Example w/ bucket name:

$ pgbackup --driver s3 Your_S3_Bucket_name postgres://database_name:1234@server_ip:80/sample

Example
`$ pgbackup --driver s3 robsonmessias1 postgres://db_rob_test:1234@3.250.212.103:80/sample`

#### Local Example w/ local path:

` $ pgbackup --driver local ./local-dump.sql postgres://db_rob_test:1234@3.250.12.200:80/sample`

Running Tests
-------------

Run tests locally using make if virtualenv is active:

`$ make`

If virtualenv isnt active then use:

`$ pipenv run make`
