[![Build Status](https://runbot.odoo.com/runbot/badge/flat/1/master.svg)](https://runbot.odoo.com/runbot)
[![Tech Doc](https://img.shields.io/badge/master-docs-875A7B.svg?style=flat&colorA=8F8F8F)](https://www.odoo.com/documentation/17.0)
[![Help](https://img.shields.io/badge/master-help-875A7B.svg?style=flat&colorA=8F8F8F)](https://www.odoo.com/forum/help-1)
[![Nightly Builds](https://img.shields.io/badge/master-nightly-875A7B.svg?style=flat&colorA=8F8F8F)](https://nightly.odoo.com/)

Odoo
----

Odoo is a suite of web based open source business apps.

The main Odoo Apps include an <a href="https://www.odoo.com/page/crm">Open Source CRM</a>,
<a href="https://www.odoo.com/app/website">Website Builder</a>,
<a href="https://www.odoo.com/app/ecommerce">eCommerce</a>,
<a href="https://www.odoo.com/app/inventory">Warehouse Management</a>,
<a href="https://www.odoo.com/app/project">Project Management</a>,
<a href="https://www.odoo.com/app/accounting">Billing &amp; Accounting</a>,
<a href="https://www.odoo.com/app/point-of-sale-shop">Point of Sale</a>,
<a href="https://www.odoo.com/app/employees">Human Resources</a>,
<a href="https://www.odoo.com/app/social-marketing">Marketing</a>,
<a href="https://www.odoo.com/app/manufacturing">Manufacturing</a>,
<a href="https://www.odoo.com/">...</a>

Odoo Apps can be used as stand-alone applications, but they also integrate seamlessly so you get
a full-featured <a href="https://www.odoo.com">Open Source ERP</a> when you install several Apps.

Getting started with Odoo
-------------------------

For a standard installation please follow the <a href="https://www.odoo.com/documentation/17.0/administration/install/install.html">Setup instructions</a>
from the documentation.

To learn the software, we recommend the <a href="https://www.odoo.com/slides">Odoo eLearning</a>, or <a href="https://www.odoo.com/page/scale-up-business-game">Scale-up</a>, the <a href="https://www.odoo.com/page/scale-up-business-game">business game</a>. Developers can start with <a href="https://www.odoo.com/documentation/17.0/developer/howtos.html">the developer tutorials</a>


## Command for Linux Ubuntu 24.04 LTS
1. Install Postgresql
    - sudo apt-get update
    - sudo apt-get install postgresql postgresql-contrib -y
    - sudo systemctl status postgresql
    - sudo -i -u postgres
    - psql
    - CREATE USER odoo WITH PASSWORD 'your_password';
    - ALTER USER odoo WITH SUPERUSER;
    - \du
    - \q
    - exit
2. Clone Repository and Setup Environment
    - git clone https://github.com/jokourno12/15labs_erp.git
    - cd 15labs_erp
    - maksure python v3.10.x: python3 --version
    - if not:
        - sudo add-apt-repository ppa:deadsnakes/ppa
        - sudo apt install python3.10 python3.10-venv python3.10-dev
        - sudo apt-get install build-essential libssl-dev libffi-dev python3-dev libsasl2-dev libldap2-dev
    - sudo python3.10 -m venv odoo-env
    - source odoo-env/bin/activate
    - pip install --upgrade pip
    - sudo apt-get install libpq-dev
    - pip install -r requirements.txt
    - sudo nano debian/odoo.conf
    - ./odoo-bin -c debian/odoo.conf