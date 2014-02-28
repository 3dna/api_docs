Donations API
==========

Resources
---------

### Donation Resource

* `amount` - amount of donation in the nation's currency
* `amount_in_cents` - amount of donation in cents
* `author_id` - id of the person who created the donation
* `billing_address` - an address resource representing the billing address
* `canceled_at` - timestamp representing when the donation was canceled
* `check_number` - check/wire/MO number
* `corporate_contribution` - true if the donation is a corporate contribution
* `created_at` - timestamp representing when the donation was created
* `donor` - a donor resource representing the donor
* `email` - the donor's email address
* `employer` - the name of the donor's employer
* `failed_at` - timestamp representing when the donation failed
* `first_name` - the donor's first name and middle name
* `id` - id of the donation
* `import_id` - id of the import job (if the donation was imported)
* `is_private` - false if the donation should not be posted publicly on the site
* `last_name` - the donor's last name
* `mailing_slug` - slug of the mailing page
* `merchant_account_id` - id of the merchant account used for paying the donation
* `ngp_id` - an id which is present if the donor has been imported from NGP VAN
* `note` - a note for this donation
* `occupation` - the donor's occupation
* `page_slug` - slug of the donation page
* `payment_type_name` - name of the [payment type](http://nationbuilder.com/what_are_the_valid_payment_types_for_imports)
* `payment_type_ngp_code` - code of the [payment type](http://nationbuilder.com/what_are_the_valid_payment_types_for_imports)
* `pledge_id` - the id of the pledge this donation fulfills.  Pledges are promises received from supporters to donate money in the future.
* `recruiter_name_or_email` - recruiter's name or email address
* `recurring_donation_id` - an id present if the donation is recurring
* `succeeded_at` - timestamp representing when the donation succeeded
* `tracking_code_slug` - tracking code for this donation
* `updated_at` - timestamp representing when the donation was last updated
* `work_address` - an address resource representing the work address

Visible only if the Voter addon is enabled:

* `actblue_order_number` - ActBlue order number
* `doing_business_with_nyc_agency` - true if affiliation is declared with an organization that does business with NYC government agencies
* `doing_business_with_nyc_business_category` - category of the business the organization does with NYC government agencies
* `fec_type` - [FEC code name](http://nationbuilder.com/what_are_the_valid_fec_codes_for_import)
* `fec_type_ngp_code` - [NGP FEC code](http://nationbuilder.com/what_are_the_valid_fec_codes_for_import)
* `election` - an election resource representing an election

### Donor Resource

* `id` - id of the person who donated
* `external_id` - string representing an external identifier for this person
* `first_name` - the person's first name and middle name
* `last_name` - the person's last name
* `email` - the person's email address
* `phone` - the person's home phone number
* `mobile` - the person's cell phone number
* `birthdate` - the person's birthdate
* `sex` - the person's sex (M or F)
* `tags` - the tags assigned to the person, as an array of strings
* `note` - a note attached to the person's profile
* `support_level` - level of support the person has for your nation, expressed as a number between 1 and 5, 1 being strong support, 5 meaning strong opposition, and 3 meaning undecided
* `home_address` - an address resource representing the person's home address
* `recruiter_id` - id of the person who recruited this person
* `created_at` - timestamp representing when the person was created
* `updated_at` - timestamp representing when the person was last updated
* `mobile_opt_in` - true if the person opted-in to mobile correspondence
* `email_opt_in` - true if the person opted-in to email correspondence
* `is_volunteer` - true if the person volunteered
* `is_twitter_follower` - true if the person is a twitter follower
* `has_facebook` - true if the person record has facebook information attached
* `state_file_id` - their id from a state voter file
* `county_file_id` - their id from a county voter file
* `nbec_guid` - their id from the NationBuilder Election Center
* `van_id` - their id from VAN
* `dw_id` - their id from Catalist
* `ngp_id` - their id from NGP
* `pf_strat_id` - their id from PoliticalForce
* `twitter_name` - twitter handle
* `twitter_id` - id from twitter
* `salesforce_id` - their id from salesforce
* `civicrm_id` - their id from CiviCRM
* `linkedin_id` - their id from LinkedIn
* `employer` - their employer's name
* `occupation` - their occupation
* `supranational_district` - district field
* `federal_district` - district field
* `labour_region` - district field
* `state_upper_district` - district field
* `state_lower_district` - district field
* `city_district` - district field
* `city_sub_district` - district field
* `county_district` - district field
* `judicial_district` - district field
* `school_district` - district field
* `school_sub_district` - district field
* `village_district` - district field
* `fire_district` - district field
* `precinct_id` - id of the precinct attached to this person, as found in the precincts API
* `party` - a one-letter code representing [provincial parties for nations](http://nationbuilder.com/support_for_international_parties)
* `rnc_id` - their id from RNC
* `rnc_regid` - their registration id from RNC

### Address Resource

* `address1` - first address line
* `address2` - second address line
* `city` - city
* `state` - state
* `zip` - zip code
* `country_code` - country code
* `lat` - latitude (using WGS-84)
* `lng` - longitude (using WGS-84)

### Election Resource

* `cycle` - election cycle
* `period` - election period
* `period_ngp_code` - [election period code](http://nationbuilder.com/what_are_the_valid_election_period_codes_for_imports)

Index Endpoint
--------------

The index endpoint provides a paginated view of the donations in a nation. 

```
GET /api/v1/donations
```

### Parameters
* `page` - result page number
* `per_page` - number of results to show on each page of results (max 100)

### Example

```
GET https://foobar.nationbuilder.com/api/v1/donations?page=2&per_page=1
```

```json
{ 
  "page": 2,
  "total_pages": 3,
  "per_page": 1,
  "total": 3,
  "results": [
      {
          "actblue_order_number": null,
          "amount": "$10.00",
          "amount_in_cents": 1000,
          "author_id": null,
          "billing_address": {
              "address1": "614 Zemlak Rds",
              "address2": null,
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
          "doing_business_with_nyc_agency": null,
          "doing_business_with_nyc_business_category": null,
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
              "city_sub_district": null,
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

### Example

Make the request:

```
POST /api/v1/donations
```

With attached body content like this:

```json 
{
  "donation": {
      "amount_in_cents": 1000,
      "first_name": "Sarah",
      "last_name": "Kerrigan",
      "payment_type_name": "Cash",
      "tracking_code_slug": "foo_bar"
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
      "doing_business_with_nyc_agency": null,
      "doing_business_with_nyc_business_category": null,
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
          "city_sub_district": null,
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
      "email": null,
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
      "recruiter_name_or_email": "Sarah Kerrigan",
      "recurring_donation_id": null,
      "succeeded_at": null,
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

### Example

Make this request (assuming you have a donation with id 89):

```
PUT /api/v1/donations/89
```

With request body like this:

```json
{
  "donation": {
      "donor": {
          "occupation": "campaign manager"
      }
  }
}
```

You will receive a response of status 200 and body response like this:

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
      "doing_business_with_nyc_agency": null,
      "doing_business_with_nyc_business_category": null,
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
          "city_sub_district": null,
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
      "occupation": "campaign manager",
      "page_slug": null,
      "payment_type_name": "Cash",
      "payment_type_ngp_code": "C",
      "pledge_id": null,
      "recruiter_name_or_email": "Sarah Kerrigan",
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
