Donations API
==========
```
In order to use the Donations API, you should first get the donor_id's (NationBuilder ID's) for the people to whom donations are to be attributed. You'll use our [People endpoints](http://nationbuilder.com/people_api) for this, such as Match, which supports a person lookup based on name, phone number or email address. If the person you'd like to attach a donation to does not already exist, you'll want to add them using the Create, Push, or Add endpoints.
```


Resources
---------

### Donation Resource

Name                      | Description                                                                                                                | Writable  | Required       | Example Value(s)
--------------------------|----------------------------------------------------------------------------------------------------------------------------|-----------|----------------|-----------------
`amount`                  | amount of donation in the nation's currency                                                                                | N         | N              | $10.00
`amount_in_cents`         | amount of donation in cents                                                                                                | Y         | Y              | 1000
`author_id`               | id of the person who created the donation                                                                                  | N         | N<sup>1</sup>  | 67
`billing_address`         | an address resource representing the billing address                                                                       | Y         | N              | (see Address Resource)
`canceled_at`             | timestamp representing when the donation was canceled                                                                      | Y         | N              | 2014-02-14T15:22:12-05:00
`check_number`            | check/wire/MO number                                                                                                       | Y         | N              | 4747392947582
`corporate_contribution`  | true if the donation is a corporate contribution                                                                           | Y         | N              | false
`created_at`              | timestamp representing when the donation was created                                                                       | N         | N              | 2014-02-14T14:36:29-05:00
`donor_id`                | the person id of the donor                                                                                                 | Y         | N<sup>2</sup>  | 8472
`donor`                   | an [abbreviated person resource](http://nationbuilder.com/people_api) representing the donor                               | N         | N              | (see Abbreviated Person Resource)
`email`                   | the donor's email address                                                                                                  | Y         | N<sup>3</sup>  | queen@swarm.net
`employer`                | the name of the donor's employer                                                                                           | Y         | N<sup>3</sup>  | ABC Consulting Co
`failed_at`               | timestamp representing when the donation failed                                                                            | Y         | N              | 2014-02-14T15:22:12-05:00
`first_name`              | the donor's first name and middle name                                                                                     | Y         | N<sup>3</sup>  | Sarah
`id`                      | id of the donation                                                                                                         | N         | N              | 314
`import_id`               | id of the import job (if the donation was imported)                                                                        | N         | N              | 890
`is_private`              | false if the donation should not be posted publicly on the site                                                            | Y         | N              | false
`last_name`               | the donor's last name                                                                                                      | Y         | N<sup>3</sup>  | Kerrigan
`mailing_slug`            | slug of the mailing page                                                                                                   | N         | N              | la_family
`merchant_account_id`     | id of the merchant account used for paying the donation                                                                    | Y         | N              | 11
`ngp_id`                  | an id which is present if the donor has been imported from NGP VAN                                                         | Y         | N              | 56
`note`                    | a note for this donation                                                                                                   | Y         | N              | very generous
`occupation`              | the donor's occupation                                                                                                     | Y         | N<sup>3</sup>  | Consultant
`page_slug`               | slug of the donation page                                                                                                  | N         | N              | ticket_sales
`payment_type_name`       | name of the [payment type](http://nationbuilder.com/what_are_the_valid_payment_types_for_imports)                          | Y         | Y<sup>4</sup>  | Check
`payment_type_ngp_code`   | code of the [payment type](http://nationbuilder.com/what_are_the_valid_payment_types_for_imports)                          | Y         | Y<sup>4</sup>  | K
`pledge_id`               | the id of the pledge this donation fulfills.  Pledges are promises received from supporters to donate money in the future. | N         | N              | 129
`recruiter_name_or_email` | recruiter's name or email address ~(will also be credited as the fundraiser for this donation)~                              | ~Y~N<sup>5</sup> | N | haydenjohns@example.com
`recurring_donation_id`   | an id present if the donation is recurring                                                                                 | N         | N<sup>6</sup>  | 89
`succeeded_at`            | timestamp representing when the donation succeeded                                                                         | Y         | N<sup>7</sup>  | 2013-02-21T10:04:15-05:00
`tracking_code_slug`      | tracking code for this donation                                                                                            | Y         | N              | vip
`updated_at`              | timestamp representing when the donation was last updated                                                                  | N         | N              | 2014-02-14T14:36:29-05:00
`work_address`            | an address resource representing the work address                                                                          | Y         | N              | (see Address Resource)

\[1\]: on the Create endpoint this field will be set to the person id of the API access token's owner.<br/>
\[2\]: it is strongly recommended to specify this field. If omitted, `email` or `first_name` and `last_name` become required and a new Person may be created.<br/>
\[3\]: use the `donor_id` field instead to specify a donor. By specifying any of these fields you override the value of the same field on the donor.<br/>
\[4\]: default: Cash (C). It is strongly recommended to specify one of these fields.<br/>
\[5\]: this field is not currently writable due to a [known bug](https://nationbuilder.com/creating_a_new_donation_through_the_api_doesn_t_carry_with_it_the_fundraiser_info)<br/>
\[6\]: this field is for internal use only.<br/>
\[7\]: if omitted the donation will be considered failed.


These fields are always visible but contain null values unless the Voter addon is enabled:

Name                      | Description                                                                        | Writable  | Required        | Example Value(s)
--------------------------|------------------------------------------------------------------------------------|-----------|-----------------|-----------------
`actblue_order_number`    | ActBlue order number                                                               | Y         | N               | 543
`fec_type`                | [FEC code name](http://nationbuilder.com/what_are_the_valid_fec_codes_for_import)  | Y         | N<sup>1</sup>   | Contribution
`fec_type_ngp_code`       | [NGP FEC code](http://nationbuilder.com/what_are_the_valid_fec_codes_for_import)   | Y         | N<sup>1</sup>   | C
`election`                | an election resource representing an election                                      | Y         | N<sup>2</sup>   | (see Election Resource)
\[1\]: default: Contribution (C). It is strongly recommended to specify one of these fields.<br/>
\[2\]: It is strongly recommended to specify this field.

### Address Resource

Name                      | Description               | Writable  | Required        | Example Value(s)
--------------------------|---------------------------|-----------|-----------------|-----------------
`address1`                | first address line        | Y         | N<sup>1</sup>   | 1600 Pennsylvania Ave
`address2`                | second address line       | Y         | N               | Suite 200
`address3`                | third address line        | Y         | N               | Apt. 207
`city`                    | city                      | Y         | N<sup>1</sup>   | Los Angeles
`state`                   | state                     | Y         | N<sup>1</sup>   | CA
`zip`                     | zip code                  | Y         | N<sup>1</sup>   | 90013
`country_code`            | country code              | Y         | N<sup>1</sup>   | US
`lat`                     | latitude (using WGS-84)   | Y         | N               | 34.0204989
`lng`                     | longitude (using WGS-84)  | Y         | N               | -118.4117325
\[1\]: It is recommended to specify these fields.

### Election Resource

Name                      | Description                                                                                           | Writable  | Required           | Example Value(s)
--------------------------|-------------------------------------------------------------------------------------------------------|-----------|--------------------|-----------------
`cycle`                   | election cycle                                                                                        | Y         | N<sup>1,2</sup>    | 2012
`period`                  | election period                                                                                       | Y         | N<sup>1,3</sup>    | General
`period_ngp_code`         | [election period code](http://nationbuilder.com/what_are_the_valid_election_period_codes_for_imports) | Y         | N<sup>1,3</sup>    | G
\[1\]: It is strongly recommended to specify `cycle` and either `period` or `period_ngp_code`.<br/>
\[2\]: default: the current election which is displayed on the Control Panel in the Political/Settings section.<br/>
\[3\]: default: Special (S) if `cycle` is defined, otherwise the value of the current election period which is displayed on the Control Panel in the Political/Settings section.

Index Endpoint
--------------

The index endpoint provides a paginated view of the donations in a nation.

```
GET /api/v1/donations
```

### Parameters
* `limit` - max number of results to show on each page of results (max 100)
* `__nonce` - generated pagination nonce. Do not modify.
* `__token` - generated pagination token. Do not modify.

### Example

```
GET https://foobar.nationbuilder.com/api/v1/donations?limit=1
```

```json
{
  "next": "/api/v1/donations?__nonce=3OUjEzI6iyybc1F3sk6YrQ&__token=ADGvBW9wM69kUiss1KqTIyVeQ5M6OwiL6ttexRFnHK9m&limit=1",
  "prev": null,
  "results": [
      {
          "actblue_order_number": null,
          "amount": "$10.00",
          "amount_in_cents": 1000,
          "author_id": null,
          "billing_address": {
              "address1": "614 Zemlak Rds",
              "address2": null,
              "address3": null,
              "city": "West Kale",
              "state": "Massachusetts",
              "country_code": "US",
              "zip": "85212-7232",
              "lat": null,
              "lng": null
          },
          "canceled_at": null,
          "check_number": null,
          "corporate_contribution": false,
          "created_at": "2014-02-14T14:36:29-05:00",
          "donor_id": 8472,
          "donor": {
              "id": 8472,
              "external_id": null,
              "support_level": null,
              "first_name": "Sarah",
              "last_name": "Kerrigan",
              "email": "queen@swarm.net",
              "phone": null,
              "mobile": null,
              "birthdate": null,
              "sex": null,
              "note": null,
              "primary_address": {
                  "address1": "614 Zemlak Rds",
                  "address2": null,
                  "address3": null,
                  "city": "West Kale",
                  "state": "Massachusetts",
                  "country_code": "US",
                  "zip": "85212-7232",
                  "lat": null,
                  "lng": null
              },
              "tags": [],
              "recruiter_id": 8472,
              "created_at": "2014-02-14T14:36:29-05:00",
              "updated_at": "2014-02-14T14:36:29-05:00",
              "mobile_opt_in": true,
              "email_opt_in": true,
              "is_volunteer": false,
              "is_twitter_follower": false,
              "has_facebook": false,
              "state_file_id": null,
              "nbec_guid": null,
              "van_id": null,
              "dw_id": null,
              "do_not_call": false,
              "do_not_contact": false,
              "ngp_id": null,
              "pf_strat_id": null,
              "county_file_id": null,
              "twitter_name": null,
              "twitter_id": null,
              "salesforce_id": null,
              "civicrm_id": null,
              "linkedin_id": null,
              "employer": "ABC Consulting Co",
              "occupation": "Consultant",
              "supranational_district": null,
              "federal_district": null,
              "labour_region": null,
              "state_upper_district": null,
              "state_lower_district": null,
              "city_district": null,
              "county_district": null,
              "judicial_district": null,
              "school_district": null,
              "school_sub_district": null,
              "village_district": null,
              "fire_district": null,
              "precinct_id": null,
              "party": null,
              "rnc_id": null,
              "rnc_regid": null
          },
          "election": {
              "cycle": "2013",
              "period": "Primary",
              "period_ngp_code": "P"
          },
          "email": "queen@swarm.net",
          "employer": "ABC Consulting Co",
          "failed_at": null,
          "fec_type": "Contribution",
          "fec_type_ngp_code": "C",
          "first_name": "Sarah",
          "id": 314,
          "import_id": null,
          "is_private": false,
          "last_name": "Kerrigan",
          "mailing_slug": null,
          "merchant_account_id": null,
          "ngp_id": null,
          "note": null,
          "occupation": "Consultant",
          "page_slug": null,
          "payment_type_name": "Check",
          "payment_type_ngp_code": null,
          "pledge_id": null,
          "recruiter_name_or_email": "Hayden Johns",
          "recurring_donation_id": null,
          "succeeded_at": "2013-02-21T10:04:15-04:00",
          "tracking_code_slug": null,
          "updated_at": "2014-02-14T14:36:29-05:00",
          "work_address": null
      }
   ]
}
```

Create Endpoint
---------------

This endpoint creates a donation with the provided data. It returns a full representation of the donation that was created. If the creation step fails, it returns an error.

```
POST /api/v1/donations
```

### Parameters

* `donation` - the resource of the donation to be created

##### Note:
* A donation is always attached to a donor. Use the Create or Match endpoints on the [People API](http://nationbuilder.com/people_api) to create or find the person who will act as the donor.
* When creating a donation, the `id` of the donor should be specified in the `donor_id` field.
* If `donor_id` is specified the following fields are copied from the donor to the donation so there is no need to specify them: `email`, `first_name`, `last_name`, `employer`, `occupation`, `recruiter_id`.
* Recurring_donation_id should not be set when creating a new donation.
* When creating a donation, if the donor's recruiter is not null then the recruiter will be credited as the fundraiser, otherwise the donor will be credited as the fundraiser. The fundraiser field is supposed to be writable via the `recruiter_name_or_email` field, but due to a known bug this does not work.

### Example

Create or find a person to whom this donation should be attached. See the [People API](http://nationbuilder.com/people_api) documentation Create and Match endpoints for examples.

Assuming you have a person with id 87, make the request:

```
POST /api/v1/donations
```

With attached body content like this:

```json
{
  "donation": {
      "amount_in_cents": 1000,
      "payment_type_name": "Cash",
      "donor_id": 87,
      "succeeded_at": "2013-02-21T10:04:15-04:00",
      "fec_type": "Contribution",
      "election": {
          "cycle": "2014",
          "period": "General",
          "period_ngp_code": "G"
      }
  }
}
```
You will receive a response of status 200, with response body like this:

```json
{
  "donation": {
      "actblue_order_number": null,
      "amount": "$10.00",
      "amount_in_cents": 1000,
      "author_id": 67,
      "billing_address": null,
      "canceled_at": null,
      "check_number": null,
      "corporate_contribution": null,
      "created_at": "2014-02-14T14:36:29-05:00",
      "donor_id": 87,
      "donor": {
          "id": 87,
          "external_id": null,
          "support_level": null,
          "first_name": "Sarah",
          "last_name": "Kerrigan",
          "email": null,
          "phone": null,
          "mobile": null,
          "birthdate": null,
          "sex": null,
          "note": null,
          "primary_address": null,
          "tags": [],
          "recruiter_id": null,
          "created_at": "2014-02-14T14:36:29-05:00",
          "updated_at": "2014-02-14T14:36:29-05:00",
          "mobile_opt_in": true,
          "email_opt_in": true,
          "is_volunteer": false,
          "is_twitter_follower": false,
          "has_facebook": false,
          "state_file_id": null,
          "nbec_guid": null,
          "van_id": null,
          "dw_id": null,
          "do_not_call": false,
          "do_not_contact": false,
          "ngp_id": null,
          "pf_strat_id": null,
          "county_file_id": null,
          "twitter_name": null,
          "twitter_id": null,
          "salesforce_id": null,
          "civicrm_id": null,
          "linkedin_id": null,
          "employer": null,
          "occupation": null,
          "supranational_district": null,
          "federal_district": null,
          "labour_region": null,
          "state_upper_district": null,
          "state_lower_district": null,
          "city_district": null,
          "county_district": null,
          "judicial_district": null,
          "school_district": null,
          "school_sub_district": null,
          "village_district": null,
          "fire_district": null,
          "precinct_id": null,
          "party": null,
          "rnc_id": null,
          "rnc_regid": null
      },
      "election": {
          "cycle": "2014",
          "period": "General",
          "period_ngp_code": "G"
      },
      "email": null,
      "employer": null,
      "failed_at": null,
      "fec_type": "Contribution",
      "fec_type_ngp_code": "C",
      "first_name": "Sarah",
      "id": 89,
      "import_id": null,
      "is_private": null,
      "last_name": "Kerrigan",
      "mailing_slug": null,
      "merchant_account_id": null,
      "ngp_id": null,
      "note": null,
      "occupation": null,
      "page_slug": null,
      "payment_type_name": "Cash",
      "payment_type_ngp_code": "C",
      "pledge_id": null,
      "recruiter_name_or_email": "Sarah Kerrigan",
      "recurring_donation_id": null,
      "succeeded_at": "2013-02-21T10:04:15-04:00",
      "tracking_code_slug": "foo_bar",
      "updated_at": "2014-02-14T14:36:29-05:00",
      "work_address": null
     }
}
```

Update Endpoint
---------------

This endpoint updates a donation with the provided id and data.  It returns a full representation of the updated donation.  If the update step fails, it returns an error.

```
PUT /api/v1/donations/:id
```

### Parameters

* `donation` - the resource attributes of the donation to change

##### Note/Warning:
* When updating a donation, the fundraiser for that donation will be set to the donor's recruiter. If the donor does not have a recruiter, then the donation will not have a fundraiser once the update is complete. This behavior is absolute and will overwrite any manual changes made in the control panel. If you rely on the fundraiser field, you should use the Donation Update endpoint with great care (or not at all).

### Example

Make this request (assuming you have a donation with id 89):

```
PUT /api/v1/donations/89
```

With request body like this:

```json
{
  "donation": {
      "amount_in_cents": 2500,
  }
}
```

You will receive a response of status 200 and body response like this:

```json
{
  "donation": {
      "actblue_order_number": null,
      "amount": "$25.00",
      "amount_in_cents": 2500,
      "author_id": 67,
      "billing_address": null,
      "canceled_at": null,
      "check_number": null,
      "corporate_contribution": null,
      "created_at": "2014-02-14T14:36:29-05:00",
      "donor_id": 87,
      "donor": {
          "id": 87,
          "external_id": null,
          "support_level": null,
          "first_name": "Sarah",
          "last_name": "Kerrigan",
          "email": "sarah@example.com",
          "phone": null,
          "mobile": null,
          "birthdate": null,
          "sex": null,
          "note": null,
          "primary_address": {
              "address1": "614 Zemlak Rds",
              "address2": null,
              "address3": null,
              "city": "West Kale",
              "state": "Massachusetts",
              "country_code": "US",
              "zip": "85212-7232",
              "lat": null,
              "lng": null
          },
          "tags": [],
          "recruiter_id": null,
          "created_at": "2014-02-14T14:36:29-05:00",
          "updated_at": "2014-02-14T14:36:29-05:00",
          "mobile_opt_in": true,
          "email_opt_in": true,
          "is_volunteer": false,
          "is_twitter_follower": false,
          "has_facebook": false,
          "state_file_id": null,
          "nbec_guid": null,
          "van_id": null,
          "dw_id": null,
          "do_not_call": false,
          "do_not_contact": false,
          "ngp_id": null,
          "pf_strat_id": null,
          "county_file_id": null,
          "twitter_name": null,
          "twitter_id": null,
          "salesforce_id": null,
          "civicrm_id": null,
          "linkedin_id": null,
          "employer": null,
          "occupation": null,
          "supranational_district": null,
          "federal_district": null,
          "labour_region": null,
          "state_upper_district": null,
          "state_lower_district": null,
          "city_district": null,
          "county_district": null,
          "judicial_district": null,
          "school_district": null,
          "school_sub_district": null,
          "village_district": null,
          "fire_district": null,
          "precinct_id": null,
          "party": null,
          "rnc_id": null,
          "rnc_regid": null
      },
      "election": null,
      "email": "sarah@example.com",
      "employer": null,
      "failed_at": null,
      "fec_type": null,
      "fec_type_ngp_code": null,
      "first_name": "Sarah",
      "id": 89,
      "import_id": null,
      "is_private": null,
      "last_name": "Kerrigan",
      "mailing_slug": null,
      "merchant_account_id": null,
      "ngp_id": null,
      "note": null,
      "occupation": null,
      "page_slug": null,
      "payment_type_name": "Cash",
      "payment_type_ngp_code": "C",
      "pledge_id": null,
      "recruiter_name_or_email": null,
      "recurring_donation_id": null,
      "succeeded_at": null,
      "tracking_code_slug": "foo_bar",
      "updated_at": "2014-05-15T10:12:11-05:00",
      "work_address": null
     }
}
```

Destroy Endpoint
----------------

This endpoint removes a donation with the provided id.  It takes no parameters and returns response code 204 on success.

```
DELETE /api/v1/donations/:id
```

Custom Fields
-------------
[Custom fields](http://nationbuilder.com/custom_fields) can be set in the API, and will also be included in all donation resource responses.

See documentation for [custom fields on the API](http://nationbuilder.com/custom_fields_api) for more details.


If you have suggestions for these docs, [they are public on Github and we accept pull requests](https://github.com/3dna/api_docs/blob/master/doc/donations_api.md).
