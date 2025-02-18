API examples
============

Here is an example to get you started with the Aiven API using curl. Replace ``{TOKEN}`` with your own value of the authentication token.

List your projects
------------------

.. code::

  curl -H "Authorization: aivenv1 {TOKEN}" https://api.aiven.io/v1/project

The following is a sample response: 

.. code:: json

    {
      "project_membership": {
        "my-best-demo": "admin",
        "aiven-sandbox": "admin"
      },
      "project_memberships": {
        "my-best-demo": [
          "admin"
        ],
        "aiven-sandbox": [
          "admin"
        ]
      },
      "projects": [
        {
          "account_id": "a225dad8d3c4",
          "account_name": "Aiven Accounts",
          "address_lines": [],
          "available_credits": "0.00",
          "billing_address": "",
          "billing_currency": "USD",
          "billing_emails": [],
          "billing_extra_text": null,
          "billing_group_id": "588a8e63-fda7-4ff7-9bff-577debfee604",
          "billing_group_name": "Billing",
          "card_info": null,
          "city": "",
          "company": "",
          "country": "",
          "country_code": "",
          "default_cloud": "google-europe-north1",
          "end_of_life_extension": {},
          "estimated_balance": "4.11",
          "estimated_balance_local": "4.11",
          "payment_method": "no_payment_expected",
          "project_name": "my-best-demo",
          "state": "",
          "tags": {},
          "tech_emails": [],
          "tenant_id": "aiven",
          "trial_expiration_time": null,
          "vat_id": "",
          "zip_code": ""
        },
        {
          "account_id": "a225dad8d3c4",
          "account_name": "Aiven Accounts",
          "address_lines": [],
          "available_credits": "0.00",
          "billing_address": "",
          "billing_currency": "USD",
          "billing_emails": [],
          "billing_extra_text": null,
          "billing_group_id": "588a8e63-fda7-4ff7-9bff-577debfee604",
          "billing_group_name": "Billing",
          "card_info": null,
          "city": "",
          "company": "",
          "country": "",
          "country_code": "",
          "default_cloud": "google-europe-north1",
          "end_of_life_extension": {},
          "estimated_balance": "4.11",
          "estimated_balance_local": "4.11",
          "payment_method": "no_payment_expected",
          "project_name": "aiven-sandbox",
          "state": "",
          "tags": {},
          "tech_emails": [],
          "tenant_id": "aiven",
          "trial_expiration_time": null,
          "vat_id": "",
          "zip_code": ""
        }
      ]
    }



List of cloud regions
---------------------

This endpoint does not require authorization; if you aren't authenticated then the standard set of clouds will be returned.

.. code::

  curl https://api.aiven.io/v1/clouds

The following is a sample response: 

.. code:: json

  {
    "clouds": [
      {
        "cloud_description": "Africa, South Africa - Amazon Web Services: Cape Town",
        "cloud_name": "aws-af-south-1",
        "geo_latitude": -33.92,
        "geo_longitude": 18.42,
        "geo_region": "africa"
      },
      {
        "cloud_description": "Africa, South Africa - Azure: South Africa North",
        "cloud_name": "azure-south-africa-north",
        "geo_latitude": -26.198,
        "geo_longitude": 28.03,
        "geo_region": "africa"
      },

For most endpoints where a cloud is used as an input, the ``cloud_name`` from this result is the field to use.

More endpoints
--------------

For more information on the available endpoints, see the `Aiven API documentation <https://api.aiven.io/doc/>`_.


