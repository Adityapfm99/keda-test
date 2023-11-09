# keda-test
[![Build Status](https://runbot.odoo.com/runbot/badge/flat/1/master.svg)](https://runbot.odoo.com/runbot)
[![Tech Doc](https://img.shields.io/badge/master-docs-875A7B.svg?style=flat&colorA=8F8F8F)](https://www.odoo.com/documentation/16.0)
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

For a standard installation please follow the <a href="https://www.odoo.com/documentation/16.0/administration/install/install.html">Setup instructions</a>
from the documentation.

To learn the software, we recommend the <a href="https://www.odoo.com/slides">Odoo eLearning</a>, or <a href="https://www.odoo.com/page/scale-up-business-game">Scale-up</a>, the <a href="https://www.odoo.com/page/scale-up-business-game">business game</a>. Developers can start with <a href="https://www.odoo.com/documentation/16.0/developer/howtos.html">the developer tutorials</a>

# ERD

# Short Video


# How to start

run : ./odoo-bin -c odoo.conf 

# Unit testing

run : ./odoo-bin -c odoo.conf -u material_test --test-enable

# CURL POSTMAN

```bash
$ Get List : 
curl --location 'http://localhost:8014/api/materials' \
--header 'x-permission-access: retry_journal' \
--header 'Cookie: frontend_lang=en_US; session_id=d13c37bc2abcca4b44dc82257ef89e1b5794e2e2' \
--data ''

```

```bash
$ Get Data By Id : 
curl --location 'http://localhost:8014/api/materials/29' \
--header 'x-permission-access: retry_journal' \
--header 'Cookie: frontend_lang=en_US; session_id=d13c37bc2abcca4b44dc82257ef89e1b5794e2e2' \
--data ''

```

```bash
$ Create : 

curl --location 'http://localhost:8014/api/materials/create' \
--header 'Content-Type: application/json' \
--header 'Cookie: frontend_lang=en_US; session_id=d13c37bc2abcca4b44dc82257ef89e1b5794e2e2; frontend_lang=en_US; session_id=d13c37bc2abcca4b44dc82257ef89e1b5794e2e2' \
--data '{
    "jsonrpc": "jsonrpc",
    "params": {
        "material_code": "P-002229",
        "material_name": "Sample Fabric",
        "material_type": "fabric",
        "material_buy_price": 190.00,
        "related_supplier": 10
    }
}

'
```

```bash
$ Update : 
curl --location 'http://localhost:8014/api/materials/update/29' \
--header 'Content-Type: application/json' \
--header 'Cookie: frontend_lang=en_US; session_id=d13c37bc2abcca4b44dc82257ef89e1b5794e2e2; frontend_lang=en_US; session_id=d13c37bc2abcca4b44dc82257ef89e1b5794e2e2' \
--data '{
    "jsonrpc": "jsonrpc",
    "params": {
        "material_code": "P-211",
        "material_name": "Sample Fabric",
        "material_type": "fabric",
        "material_buy_price": 190.00,
        "related_supplier": 10
    }
}

'
```

```bash
$ Delete By Id : 
curl --location 'http://localhost:8014/api/materials/delete/29' \
--header 'Content-Type: application/json' \
--header 'Cookie: frontend_lang=en_US; session_id=d13c37bc2abcca4b44dc82257ef89e1b5794e2e2' \
--data '{
    "jsonrpc": "jsonrpc",
    "params": {
        "material_code": "P-009",
        "material_name": "Sample Fabric",
        "material_type": "fabric",
        "material_buy_price": 190.00,
        "related_supplier": 10
    }
}

'
```