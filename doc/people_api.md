People API
==========

Resources
---------

### Person Resource

* `active_customer_expires_at` - the date at which to consider a customer no longer active
* `active_customer_started_at` - the date from which a customer is considered active
* `author_id` - the resource ID of the person who created this person in the nation
* `author` -  an abbreviated person resource representing the person who created this person’s record
* `auto_import_id` - the ID given to a signup when a person is auto imported
* `availability` - date and time this person is available (such as for volunteer shifts)
* `ballots` - an array of ballot resources representing votes in elections
* `banned_at` - the time and date this person was banned
* `billing_address` - an address resource representing this person’s billing address
* `bio` - the bio information that this person provided on their public profile via the “short bio” field
* `birthdate` - this person's birth date
* `call_status_id` - the ID of the call status associated with this person
* `call_status_name` - the name of the call status associated with this person
* `capital_amount_in_cents` - the balance of this person’s political or social capital, in cents
* `children_count` - the number of people assigned to this person
* `church` - the church that this person goes to
* `city_district` - district field
* `city_sub_district` - district field
* `civicrm_id` - this person’s ID from CiviCRM
* `closed_invoices_amount_in_cents` - the aggregate amount of all this person’s closed invoices in cents
* `closed_invoices_count` - the number of closed invoices associated with this person
* `contact_status_id` - ID of a contact status associated with this person. Possible values: 1: answered, 2: bad_info, 9: inaccessible, 3: left_message, 4: meaningful_interaction, 6: not_interested, 7: no_answer, 8: refused, 5: send_information, 0: other
* `contact_status_name` - name of a contact status associated with this person: Possible values: answered, bad_info, inaccessible, left_message, meaningful_interaction, not_interested, no_answer, refused, send_information, other
* `could_vote_status` - boolean indicating if this person could vote in an election or not, derived from their election-related IDs
* `county_district` - district field
* `county_file_id` - this person’s ID from a county voter file
* `created_at` - timestamp representing when this person was created in the nation
* `demo` - Asian, Black, Hispanic, White, Other, Unknown
* `do_not_call` - this is a boolean flag that lets us know if this person is on a do not call list
* `do_not_contact` - this is a boolean flag that lets us know if this person is on a do not contact list
* `donations_amount_in_cents` - aggregate amount of all this person’s donations in cents
* `donations_amount_this_cycle_in_cents` - the aggregate value of the donations this person made this cycle in cents
* `donations_count_this_cycle` - the number of donations this person made this cycle
* `donations_count` - the total number of donations made by this person
* `donations_pledged_amount_in_cents` - the aggregate amount of the donations pledged by this person in cents
* `donations_raised_amount_in_cents` - the aggregate amount of the donations raised by this person in cents, including their own donations
* `donations_raised_amount_this_cycle_in_cents` - the aggregate value of all donations raised this cycle by this person, including their own
* `donations_raised_count_this_cycle` - the number of donations raised this cycle by this person, including their own
* `donations_raised_count` - the total number of donations raised
* `donations_to_raise_amount_in_cents` - the goal amount of donations for this person to raise in cents
* `dw_id` - this person’s ID from Catalist
* `email1_is_bad` - boolean indicating if email1 for this person is bad
* `email1` - an email address for this person
* `email2_is_bad` - boolean indicating if email2 for this person is bad
* `email2` - an email address for this person
* `email3_is_bad` - boolean indicating if email3 for this person is bad
* `email3` - an email address for this person
* `email4_is_bad` - boolean indicating if email4 for this person is bad
* `email4` - an email address for this person
* `email_opt_in` - boolean representing whether this person has opted-in to email correspondence
* `email` - when reading this field clients can expect the person's best email address to be returned. A person can have up to 4 email addresses: `email1`, `email2`, `email3` and `email4`. The best email address is the one that is not marked as bad and is also marked as primary, that is, it is referenced by the `primary_email_id` field. When writing this field, its value will be assigned to one of `email1`, `email2`, `email3` and `email4` and it will be marked as primary. If all 4 email fields are already populated then the first one marked as bad will be overwritten. If none of the 4 email fields are marked as bad then the value of `email` will be dropped. In this case one of the 4 email fields and the `primary_email_id` have to be directly updated.
* `employer` - the name of the company for which this person works
* `ethnicity` - the ethnicity of this person as free text
* `external_id` - a string representing an external identifier for this person
* `facebook_address` - this person’s address based on their Facebook profile
* `facebook_profile_url` - the URL of this person’s Facebook profile
* `facebook_updated_at` - the date and time this person's Facebook info was last updated
* `facebook_username` - this person's Facebook username
* `fax_number` - the fax number associated with this person
* `federal_district` - district field
* `federal_donotcall` - boolean value indicating if this user is on the U.S. Federal Do Not Call list
* `fire_district` - district field
* `first_donated_at` - date and time of this person's first donation
* `first_fundraised_at` -  date and time that this person first raised donation
* `first_invoice_at` - date and time of this person's first invoice
* `first_name` - the person's first name and middle names
* `first_prospect_at` - date and time that this user first became a prospect
* `first_recruited_at` - date and time that this user was first recruited
* `first_supporter_at` - date and time that this user became a supporter for the first time
* `first_volunteer_at` - date and time that this person first volunteered
* `full_name` - this person’s full name
* `has_facebook` - a boolean representing whether this person has Facebook information
* `home_address` - an address resource representing the home address
* `id` - the NationBuilder ID of the person, specific to the authorized nation
* `import_id` - the ID associated with this person when they were imported
* `inferred_party` - the party the person is believed to be associated with
* `inferred_support_level` - a possible support level
* `invoice_payments_amount_in_cents` - total invoice payment amount (cents)
* `invoice_payments_referred_amount_in_cents` - the aggregate amount of invoice payments made by recruits of this person (cents)
* `invoices_amount_in_cents` - the aggregate amount of all of this person’s invoices (cents)
* `invoices_count` - the number of invoices this person has
* `is_absentee_voter` - a boolean field that indicates if the person votes absentee
* `is_active_voter` - a boolean field that indicates if the person is actively voting
* `is_deceased` - a boolean field that indicates if the person is alive or not
* `is_donor` - a boolean field that indicates if the person has donated
* `is_early_voter` - a boolean field that indicates if the person votes early
* `is_fundraiser` - a boolean value that indicates if this person has previously fundraised
* `is_ignore_donation_limits` - a boolean that indicates whether this person is not subject to donation limits associated with the nation
* `is_leaderboardable` - a boolean that tells if this person is allowed to show up on the leaderboard
* `is_mobile_bad` - a boolean reflecting whether this person’s cell number is invalid
* `is_permanent_absentee_voter` - a boolean field that indicates if the person has registered as a permanent absentee voter
* `is_possible_duplicate` - a boolean field that indicates if the NationBuilder matching algorithm thinks this person is a match to someone else in the nation
* `is_profile_private` - a boolean that tells if this person’s profile is private
* `is_profile_searchable` - a boolean that tells if this person’s profile is allowed to show up in search results
* `is_prospect` - a boolean field that indicates if this person is a prospect
* `is_supporter` - a boolean field that indicates if this person is a supporter
* `is_survey_question_private` - a boolean field that indicates if this person’s survey responses are private
* `is_twitter_follower` - whether the person is a Twitter follower of one of the nation’s broadcasters
* `is_volunteer` - a boolean field that indicates whether the person has volunteered
* `judicial_district` - a district field
* `labour_region` - a district field
* `language` - this person’s primary language
* `last_call_id` - the id of the last contact to this person
* `last_contacted_at` - the time and date of the last time this person was contacted
* `last_contacted_by` - an abbreviated person resource representing the last user who contacted this person
* `last_donated_at` - the time and date of this person’s last donation
* `last_fundraised_at` - the time and date of the last time this person fundraised
* `last_invoice_at` - the time and date of this person’s last invoice
* `last_name` - this person's last name
* `last_rule_violation_at` - the time and date of this person’s last rule violation
* `legal_name` - the full (legal) name of this person
* `linkedin_id` - this person’s ID from LinkedIn
* `locale` - the ISO locale that the user has their administrative account set to (US, ES, FR etc.)
* `mailing_address` - an address resource representing the mailing address
* `marital_status` - the person’s [marital status](http://nationbuilder.com/what_are_the_codes_for_marital_status_on_imports)
* `media_market_name` - the name of this person’s media market
* `meetup_address` - an address resource based on this person’s profile in Meetup
* `membership_expires_at` - the time and date that this user’s membership expires
* `membership_level_name` - the name of the level of this person’s membership
* `membership_started_at` - the time and date that this user started a membership
* `middle_name` - this person’s middle name
* `mobile_normalized` - this person's cell phone number in normalized form
* `mobile_opt_in` - a boolean representing whether the person has opted-in to mobile correspondence
* `mobile` - this person's cell phone number
* `nbec_guid` - this person’s ID from the NationBuilder Election Center
* `nbec_precinct_code` - the unique identifier assigned to this person in the NationBuilder Election Center
* `ngp_id` - this person’s ID from NGP
* `note_updated_at` - the date and time the note attached to this person was updated
* `note` - a note to attach to the person's profile
* `occupation` - the type of work this person does
* `outstanding_invoices_amount_in_cents` - the aggregate value of all this person’s outstanding invoices in cents
* `outstanding_invoices_count` - the number of outstanding invoices this person has
* `overdue_invoices_count` - the number of overdue invoices this person has
* `page_slug` - the page this person first signed up from
* `parent_id` - the NationBuilder ID of this person’s point person
* `parent` - an abbreviated person resource representing this person’s point person
* `party_member` - a boolean that tells if this person is a member of a political party
* `party` - a one-letter code representing [provincial parties for nations](http://nationbuilder.com/support_for_international_parties)
* `pf_strat_id` - a person’s historical ID from PoliticalForce
* `phone_normalized` - this person's home phone number in normalized form
* `phone_time` - the time that has been selected as the best time to call this person
* `phone` - this person's home phone number
* `precinct_code` - the code of the precinct that this person lives in
* `precinct_id` - the ID of the precinct associated with this person
* `precinct_name` - the name of the precinct that this person votes in
* `prefix` - the name prefix of this person, i.e. Mr., Mrs.
* `previous_party` - the party this person had selected before their current party selection
* `primary_address` - an address resource representing the primary address
* `primary_email_id` - the id of the primary email address associated with this person, one of: 1, 2, 3 or 4. This id corresponds to the 4 email addresses a person can have: `email1`, `email2`, `email3` and `email4`.
* `priority_level_changed_at` - the date and time that this person’s priority level changed
* `priority_level` - the priority level associated with this person
* `profile_content_html` - the profile content for this person’s public profile in HTML
* `profile_content` - the content for this person’s public profile
* `profile_headline` - the headline for this person’s public profile
* `received_capital_amount_in_cents` - the aggregate amount of political capital ever received by this person
* `recruiter_id` - the ID of the person who recruited this person
* `recruiter` - an abbreviated person resource representing the person who recruited this person
* `recruits_count` - the number of people that were recruited by this person
* `registered_address` - an address resource representing the registered address
* `registered_at` - the date this person registered to become a voter
* `religion` - this person’s religion
* `rnc_id` - this person’s ID from the RNC
* `rnc_regid` - this person’s registration ID from the RNC
* `rule_violations_count` - the number of times this person has violated one of the nation’s rules
* `salesforce_id` - this person’s ID from Salesforce
* `school_district` - a district field
* `school_sub_district` - a district field
* `sex` - this person's gender (M, F or O)
* `signup_type` - '0' for person, '1' for organization
* `spent_capital_amount_in_cents` - the aggregate amount of capital ever spent by this person (in cents)
* `state_file_id` - this person’s ID from a state voter file
* `state_lower_district` - a district field
* `state_upper_district` - a district field
* `submitted_address` - the address this person submitted
* `subnations` - an array of subnations that this person belongs to
* `suffix` - the suffix this person uses w/their name, i.e. Jr., Sr. or III
* `support_level_changed_at` - the time and date that this person’s support level changed
* `support_level` - the level of support this person has for your nation, expressed as a number between 1 and 5, 1 being Strong support, 5 meaning strong opposition, and 3 meaning undecided.
* `support_probability_score` - the likelihood that this person will support you at election time
* `supranational_district` - district field
* `tags` - the tags assigned to this person, as an array of strings
* `turnout_probability_score` - the probability that this person will turn out to vote
* `twitter_address` - this person’s location based on their Twitter profile
* `twitter_description` - the description that this person provided in their Twitter profile
* `twitter_followers_count` - the number of followers this person has on Twitter
* `twitter_friends_count` - the number of friends this person has on Twitter
* `twitter_id` - this person’s ID from Twitter
* `twitter_location` - an address resource representing this person’s address based on Twitter’s location data
* `twitter_login` - this person’s Twitter login name
* `twitter_name` - this person’s Twitter handle, e.g. FoobarSoftwares
* `twitter_updated_at` - the last time this person’s Twitter record was updated
* `twitter_website` - the URL of the website that this person included in their Twitter profile
* `unsubscribed_at` - the date/time that this person unsubscribed from emails
* `updated_at` - the timestamp representing when this person was last updated
* `user_submitted_address` - an address resource representing the address this person submitted
* `username` - this person’s NationBuilder username
* `van_id` - this person’s ID from VAN
* `village_district` - a district field
* `voter_updated_at` - the last time voter data was gathered for this person
* `ward` - district field
* `warnings_count` - the number of warnings this person has received
* `website` - the URL of this person’s website
* `work_address` - an address resource representing this person’s work address
* `work_phone_number` - a work phone number for this person


### Abbreviated Person Resource

* `birthdate` - this person's birth date
* `city_district` - district field
* `civicrm_id` - this person’s ID from CiviCRM
* `county_district` - district field
* `county_file_id` - this person’s ID from a county voter file
* `created_at` - timestamp representing when this person was created in the nation
* `do_not_call` - this is a boolean flag that lets us know if this person is on a do not call list
* `do_not_contact` - this is a boolean flag that lets us know if this person is on a do not contact list
* `dw_id` - this person’s ID from Catalist
* `email_opt_in` - boolean representing whether this person has opted-in to email correspondence
* `email` - the person's email address if reading or writing a single address
* `employer` - the name of the company for which this person works
* `external_id` - a string representing an external identifier for this person
* `federal_district` - district field
* `fire_district` - district field
* `first_name` - the person's first name and middle names
* `has_facebook` - a boolean representing whether this person has Facebook information
* `id` - the NationBuilder ID of the person, specific to the authorized nation
* `is_twitter_follower` - whether the person is a Twitter follower of one of the nation’s broadcasters
* `is_volunteer` - a boolean field that indicates whether the person has volunteered
* `judicial_district` - district field
* `labour_region` - district field
* `last_name` - this person's last name
* `linkedin_id` - this person’s ID from LinkedIn
* `mobile_opt_in` - a boolean representing whether the person has opted-in to mobile correspondence
* `mobile` - this person's cell phone number
* `nbec_guid` - this person’s ID from the NationBuilder Election Center
* `ngp_id` - this person’s ID from NGP
* `note` - a note to attach to the person's profile
* `occupation` - the type of work this person does
* `party` - a one-letter code representing [provincial parties for nations](http://nationbuilder.com/support_for_international_parties)
* `pf_strat_id` - a person’s historical ID from PoliticalForce
* `phone` - this person's home phone number
* `precinct_id` - the ID of the precinct associated with this person
* `primary_address` - an address resource representing the primary address
* `recruiter_id` - the ID of the person who recruited this person
* `rnc_id` - this person’s ID from the RNC
* `rnc_regid` - this person’s registration ID from the RNC
* `salesforce_id` - this person’s ID from Salesforce
* `school_district` - district field
* `school_sub_district` - district field
* `sex` - this person's gender (M, F or O)
* `state_file_id` - this person’s ID from a state voter file
* `state_lower_district` - district field
* `state_upper_district` - district field
* `support_level` - the level of support this person has for your nation, expressed as a number between 1 and 5, 1 being Strong support, 5 meaning strong opposition, and 3 meaning undecided.
* `supranational_district` - district field
* `tags` - the tags assigned to this person, as an array of strings
* `twitter_id` - this person’s ID from Twitter
* `twitter_name` - this person’s Twitter handle, e.g. FoobarSoftwares
* `updated_at` - the timestamp representing when this person was last updated
* `van_id` - this person’s ID from VAN
* `village_district` - district field
* `ward` - district field


### Address Resource

* `address1` - first address line
* `address2` - second address line
* `address3` - third address line
* `city` - city
* `state` - state
* `zip` - zip code
* `country_code` - country code
* `lat` - latitude (using WGS-84)
* `lng` - longitude (using WGS-84)

### Ballot Resource

* `cast_at` - when the ballot was cast,
* `country_code` - country code for the country the ballot was cast (required),
* `election_at` - when the election was held (required),
* `election_period` - the type of election (General, Primary, Presidential Primary, or Special, not case sensitive, not required for international elections),
* `party` - party for primary elections (American Independent, Americans Elect, Communist, Conservative, Constitution, Constituional, Democrat, Federalist, Green, Green Rainbow, Independent, Justice, La Raza, Labor, Liberal, Libertarian, Marijuana, Moderate, Natural Law, Other, Peace And Freedom, Pirate, Reform, Republican, Right To Life, Socialist, Undeclared, Whig, Working Families),
* `state` - which state the election was held in (required for US elections),
* `vote_method` - how the ballot was cast (required)

Count Endpoint
--------------

The count endpoint provides a total count of all the people in the nation.

```
GET /api/v1/people/count
```

### Example

```
GET https://foobar.nationbuilder.com/api/v1/people/count
```

```json
{
  "people_count": 90013
}
```

Index Endpoint
--------------

The index endpoint provides a paginated view of the people in a nation.  Each person's data is abbreviated for the Index view. To get a full representation use the Show endpoint

```
GET /api/v1/people
```

### Parameters
* `limit` - max number of results to show in one page of results (default 10, max 100).
* `__nonce` - generated pagination nonce. Do not modify.
* `__token` - generated pagination token. Do not modify.

### Example

```
GET https://foobar.nationbuilder.com/api/v1/people
```

```json
{
  "next": "/api/v1/people?__nonce=3OUjEzI6iyybc1F3sk6YrQ&__token=ADGvBW9wM69kUiss1KqTIyVeQ5M6OwiL6ttexRFnHK9m",
  "prev": null,
  "results": [
    {
      "birthdate": "1973-04-04",
      "city_district": null,
      "civicrm_id": 7,
      "county_district": "11",
      "county_file_id": "97076395",
      "created_at": "2014-02-02T11:51:23-05:00",
      "do_not_call": false,
      "do_not_contact": false,
      "dw_id": null,
      "email": "festeban@example.com",
      "email_opt_in": true,
      "employer": "Sun Film Foundation",
      "external_id": "781986",
      "federal_district": "0",
      "fire_district": null,
      "first_name": "Fernando",
      "has_facebook": false,
      "id": 453,
      "is_twitter_follower": false,
      "is_volunteer": false,
      "judicial_district": null,
      "labour_region": null,
      "last_name": "Esteban",
      "linkedin_id": null,
      "mobile": "5738882938",
      "mobile_opt_in": true,
      "nbec_guid": "000099dc-00f0-11e2-b349-27c4eb6c1979",
      "ngp_id": null,
      "note": "Has 3 kids. Ask about the baby on the way",
      "occupation": "Community Organizer",
      "party": "P",
      "pf_strat_id": 91207702,
      "phone": "2156726335",
      "precinct_id": null,
      "primary_address": {
        "address1": "448 S Hill St",
        "address2": "Suite 200",
        "address3": null,
        "city": "Los Angeles",
        "state": "CA",
        "country_code": "US",
        "zip": "90013",
        "lat": 34.0502,
        "lng": -117.2478
      },
      "recruiter_id": null,
      "rnc_id": 2653431,
      "rnc_regid": "003F4ED9-3C5C-4E15-8178-B84920F41BFF",
      "salesforce_id": null,
      "school_district": "Chicago Public Schools",
      "school_sub_district": null,
      "sex": "F",
      "signup_type": 0,
      "state_file_id": "100000012",
      "state_lower_district": "024",
      "state_upper_district": "1",
      "support_level": 1,
      "supranational_district": "Eastern Euro Region",
      "tags": [],
      "twitter_id": "63403772",
      "twitter_name": "AngryPig",
      "updated_at": "2014-02-02T11:51:23-05:00",
      "van_id": "2",
      "village_district": null
    },
    {
      "birthdate": "1943-03-06",
      "city_district": null,
      "civicrm_id": 9,
      "county_district": "12",
      "county_file_id": "27376395",
      "created_at": "2014-02-02T11:51:23-05:00",
      "do_not_call": false,
      "do_not_contact": false,
      "dw_id": null,
      "email": "alice@example.com",
      "email_opt_in": true,
      "employer": "Moon Film Foundation",
      "external_id": "381986",
      "federal_district": "0",
      "fire_district": null,
      "first_name": "Alice",
      "has_facebook": false,
      "id": 672,
      "is_twitter_follower": false,
      "is_volunteer": false,
      "judicial_district": null,
      "labour_region": null,
      "last_name": "Cooper",
      "linkedin_id": null,
      "mobile": "1242882938",
      "mobile_opt_in": true,
      "nbec_guid": "000088dc-00f0-11e2-b349-27c4eb6c1979",
      "ngp_id": null,
      "note": "Still single.",
      "occupation": "Community Organizer",
      "party": "P",
      "pf_strat_id": 21207702,
      "phone": "9216726335",
      "precinct_id": null,
      "primary_address": {
          "address1": "High St",
          "address2": "Apt 2312",
          "address3": "Suite 5A",
          "city": "Dallas",
          "state": "TX",
          "country_code": "US",
          "zip": "23891",
          "lat": 34.0502,
          "lng": -117.2478
      },
      "recruiter_id": null,
      "rnc_id": 2652231,
      "rnc_regid": "002D2ED9-3C5C-4E15-8178-B84920F41BFF",
      "salesforce_id": null,
      "school_district": "Dallas Public Schools",
      "school_sub_district": null,
      "sex": "F",
      "signup_type": 0,
      "state_file_id": "100000013",
      "state_lower_district": "024",
      "state_upper_district": "1",
      "support_level": 1,
      "supranational_district": "Scotland Euro Region",
      "tags": [],
      "twitter_id": "13203772",
      "twitter_name": "AngryBird",
      "updated_at": "2014-02-02T11:51:23-05:00",
      "van_id": "2",
      "village_district": null
    }
  ]
}
```

Show Endpoint
-------------

The Show endpoint returns a full representation of the person with the provided id.  It takes no parameters.

```
GET /api/v1/people/:id
```

### Parameters

* `id_type` - type of id to use, set to 'external' to show the person based on their external id

### Example

Make a request like this:

```
GET /api/v1/people/672
```

or this:

```
GET /api/v1/people/8491?id_type=external
```

You will receive a response of status 200, with response body like this:

```json
{
  "person": {
    "birthdate": "1973-04-04",
    "city_district": "city_district_1",
    "civicrm_id": 123489,
    "county_district": "county_district_1",
    "county_file_id": "mycountyfileid",
    "created_at": "2014-02-02T11:51:23-05:00",
    "do_not_call": false,
    "do_not_contact": false,
    "dw_id": 987,
    "email": "test@example.com",
    "email_opt_in": true,
    "employer": "Texas Instruments",
    "external_id": "8491",
    "federal_district": "federal_district_1",
    "fire_district": "fire_district_1",
    "first_name": "Bob",
    "has_facebook": true,
    "id": 672,
    "is_twitter_follower": false,
    "is_volunteer": false,
    "judicial_district": "judicial_district_1",
    "labour_region": "labour_region_1",
    "last_name": "Smith",
    "linkedin_id": "linkedinid",
    "mobile": "5738882938",
    "mobile_opt_in": true,
    "nbec_guid": "c4545",
    "ngp_id": "myngpid",
    "note": "Has 3 kids. Ask about the baby on the way",
    "occupation": "Programmer",
    "party": "P",
    "pf_strat_id": 876,
    "phone": "2156726335",
    "precinct_id": 21,
    "primary_address": null,
    "recruiter_id": 3421,
    "rnc_id": 1234567,
    "rnc_regid": "003F4ED9-3C5C-4E15-8178-B84920F41BFF",
    "salesforce_id": "salesforceid",
    "school_district": "school_district_1",
    "school_sub_district": "school_sub_district_1",
    "sex": "F",
    "signup_type": 0,
    "state_file_id": "a12345z",
    "state_lower_district": "state_lower_district_1",
    "state_upper_district": "state_upper_district_1",
    "support_level": 1,
    "supranational_district": "region_abc",
    "tags": [],
    "twitter_id": "765",
    "twitter_name": "AngryPig",
    "updated_at": "2014-02-02T11:51:23-05:00",
    "van_id": "d6767",
    "village_district": "village_district_1",
    "active_customer_expires_at": null,
    "active_customer_started_at": null,
    "author": null,
    "author_id": null,
    "auto_import_id": null,
    "availability": "anytime",
    "banned_at": null,
    "billing_address": null,
    "bio": "Specialist in management and business growth.",
    "call_status_id": 5,
    "call_status_name": "no-answer",
    "capital_amount_in_cents": 0,
    "children_count": 2,
    "church": "Liberty Church",
    "city_sub_district": "DOWNTOWN LOS ANGELES",
    "closed_invoices_amount_in_cents": null,
    "closed_invoices_count": null,
    "contact_status_id": 3,
    "contact_status_name": "Answered",
    "could_vote_status": 1,
    "demo": "W",
    "donations_amount_in_cents": 0,
    "donations_amount_this_cycle_in_cents": 0,
    "donations_count": 0,
    "donations_count_this_cycle": 0,
    "donations_pledged_amount_in_cents": 0,
    "donations_raised_amount_in_cents": 0,
    "donations_raised_amount_this_cycle_in_cents": 0,
    "donations_raised_count": 0,
    "donations_raised_count_this_cycle": 0,
    "donations_to_raise_amount_in_cents": 0,
    "email1": "test@example.com",
    "email1_is_bad": false,
    "email2": null,
    "email2_is_bad": false,
    "email3": null,
    "email3_is_bad": false,
    "email4": null,
    "email4_is_bad": false,
    "ethnicity": null,
    "facebook_address": null,
    "facebook_profile_url": "http://www.facebook.com/profile.php?id=124071",
    "facebook_updated_at": "2014-02-25T11:22:12-04:00",
    "facebook_username": "alice",
    "fax_number": null,
    "federal_donotcall": false,
    "first_donated_at": "2013-02-02T11:51:23-05:00",
    "first_fundraised_at": "2013-04-02T11:51:23-05:00",
    "first_invoice_at": "2013-01-02T11:51:23-05:00",
    "first_prospect_at": "2013-11-02T11:51:23-05:00",
    "first_recruited_at": "2013-05-02T11:51:23-05:00",
    "first_supporter_at": "2014-02-02T11:51:23-05:00",
    "first_volunteer_at": "2013-05-02T11:51:23-05:00",
    "full_name": "Bob Smith",
    "home_address": null,
    "import_id": null,
    "inferred_party": "H",
    "inferred_support_level": 1,
    "invoice_payments_amount_in_cents": 0,
    "invoice_payments_referred_amount_in_cents": 0,
    "invoices_amount_in_cents": null,
    "invoices_count": null,
    "is_deceased": false,
    "is_donor": false,
    "is_fundraiser": false,
    "is_ignore_donation_limits": false,
    "is_leaderboardable": true,
    "is_mobile_bad": false,
    "is_possible_duplicate": false,
    "is_profile_private": false,
    "is_profile_searchable": true,
    "is_prospect": false,
    "is_supporter": true,
    "is_survey_question_private": false,
    "language": "EN",
    "last_call_id": 2378,
    "last_contacted_at": null,
    "last_contacted_by": null,
    "last_donated_at": "2014-02-02T11:51:23-05:00",
    "last_fundraised_at": "2014-01-01T11:51:23-05:00",
    "last_invoice_at": null,
    "last_rule_violation_at": null,
    "legal_name": null,
    "locale": "en",
    "mailing_address": null,
    "marital_status": "S",
    "media_market_name": null,
    "meetup_address": null,
    "membership_expires_at": null,
    "membership_level_name": null,
    "membership_started_at": null,
    "middle_name": "T.",
    "mobile_normalized": null,
    "nbec_precinct_code": null,
    "note_updated_at": "2014-01-01T11:51:23-05:00",
    "outstanding_invoices_amount_in_cents": null,
    "outstanding_invoices_count": null,
    "overdue_invoices_count": 0,
    "page_slug": null,
    "parent": null,
    "parent_id": null,
    "party_member": false,
    "phone_normalized": null,
    "phone_time": "daytime",
    "precinct_code": "9876",
    "precinct_name": "9876",
    "prefix": null,
    "previous_party": "U",
    "primary_email_id": 1,
    "priority_level": 4,
    "priority_level_changed_at": null,
    "profile_content": "I support Abraham Lincoln for President.",
    "profile_content_html": "<p>I support Abraham Lincoln for President.</p>",
    "profile_headline": "Abe is back!",
    "received_capital_amount_in_cents": 0,
    "recruiter": {
      "birthdate": "1962-03-03",
      "city_district": null,
      "civicrm_id": 9,
      "county_district": "11",
      "county_file_id": "97076395",
      "created_at": "2014-02-02T11:51:23-05:00",
      "do_not_call": false,
      "do_not_contact": false,
      "dw_id": null,
      "email": null,
      "email_opt_in": true,
      "employer": "Sun Film Foundation",
      "external_id": "781986",
      "federal_district": "0",
      "fire_district": null,
      "first_name": "Mina",
      "has_facebook": false,
      "id": 3421,
      "is_twitter_follower": false,
      "is_volunteer": false,
      "judicial_district": null,
      "labour_region": null,
      "last_name": "Abbott",
      "linkedin_id": null,
      "mobile": "5738882938",
      "mobile_opt_in": true,
      "nbec_guid": "000099dc-00f0-11e2-b349-27c4eb6c1979",
      "ngp_id": null,
      "note": "Has 3 kids. Ask about the baby on the way",
      "occupation": "Community Organizer",
      "party": "P",
      "pf_strat_id": 91207702,
      "phone": "2156726335",
      "precinct_id": null,
      "primary_address": null,
      "recruiter_id": null,
      "rnc_id": 2653431,
      "rnc_regid": "003F4ED9-3C5C-4E15-8178-B84920F41BFF",
      "salesforce_id": null,
      "school_district": "Chicago Public Schools",
      "school_sub_district": null,
      "sex": "F",
      "signup_type": 0,
      "state_file_id": "100000012",
      "state_lower_district": "024",
      "state_upper_district": "1",
      "support_level": 1,
      "supranational_district": "Eastern Euro Region",
      "tags": [],
      "twitter_id": "63403772",
      "twitter_name": "AngryPig",
      "updated_at": "2014-02-02T11:51:23-05:00",
      "van_id": "2",
      "village_district": null
    },
    "recruits_count": 0,
    "registered_address": null,
    "registered_at": null,
    "religion": null,
    "rule_violations_count": 0,
    "spent_capital_amount_in_cents": 0,
    "submitted_address": "123 Main St Portland, ME 04101",
    "subnations": ["abeforprez", "operalovers"],
    "suffix": null,
    "support_level_changed_at": "2014-02-02T11:51:23-05:00",
    "support_probability_score": null,
    "turnout_probability_score": null,
    "twitter_address": null,
    "twitter_description": "Animal lover.",
    "twitter_followers_count": 564,
    "twitter_friends_count": 32,
    "twitter_location": "Dallas, TX",
    "twitter_login": "trinity",
    "twitter_updated_at": "2014-01-01T11:51:23-05:00",
    "twitter_website": "http://mytwittersite.com",
    "unsubscribed_at": null,
    "user_submitted_address": null,
    "username": null,
    "warnings_count": 0,
    "website": null,
    "work_address": null,
    "work_phone_number": null
  },
  "precinct": {
    "id": 21,
    "code": "9876",
    "name": "9876"
  }
}
```

Match Endpoint
--------------

Use the match endpoint to find people that have certain attributes.  A single person must match the given criteria for this endpoint to return success.

```
GET /api/v1/people/match
```

### Parameters
Parameters act as matching criteria.

* `email` - email address
* `first_name` - first name
* `last_name` - last name
* `phone` - phone number
* `mobile` - mobile number

### Example

Make the request:

```
GET https://foobar.nationbuilder.com/api/v1/people/match?email=test@example.com
```

You will receive a response with a body like this if the person exists:

```json
{
    "person": {
        "birthdate": "1973-04-04",
        "city_district": "city_district_1",
        "civicrm_id": 123489,
        "county_district": "county_district_1",
        "county_file_id": "mycountyfileid",
        "created_at": "2014-02-02T11:51:23-05:00",
        "do_not_call": false,
        "do_not_contact": false,
        "dw_id": 987,
        "email": "test@example.com",
        "email_opt_in": true,
        "employer": "Texas Instruments",
        "external_id": "external",
        "federal_district": "federal_district_1",
        "fire_district": "fire_district_1",
        "first_name": "Bob",
        "has_facebook": true,
        "id": 98,
        "is_twitter_follower": false,
        "is_volunteer": false,
        "judicial_district": "judicial_district_1",
        "labour_region": "labour_region_1",
        "last_name": "Smith",
        "linkedin_id": "linkedinid",
        "mobile": "5738882938",
        "mobile_opt_in": true,
        "nbec_guid": "c4545",
        "ngp_id": "myngpid",
        "note": "Has 3 kids. Ask about the baby on the way",
        "occupation": "Programmer",
        "party": "P",
        "pf_strat_id": 876,
        "phone": "2156726335",
        "precinct_id": 77,
        "primary_address": null,
        "recruiter_id": 233,
        "rnc_id": 1234567,
        "rnc_regid": "003F4ED9-3C5C-4E15-8178-B84920F41BFF",
        "salesforce_id": "salesforceid",
        "school_district": "school_district_1",
        "school_sub_district": "school_sub_district_1",
        "sex": "F",
        "signup_type": 0,
        "state_file_id": "a12345z",
        "state_lower_district": "state_lower_district_1",
        "state_upper_district": "state_upper_district_1",
        "support_level": 1,
        "supranational_district": "region_abc",
        "tags": [],
        "twitter_id": "765",
        "twitter_name": "AngryPig",
        "updated_at": "2014-02-02T11:51:23-05:00",
        "van_id": "d6767",
        "village_district": "village_district_1",
        "active_customer_expires_at": null,
        "active_customer_started_at": null,
        "author": null,
        "author_id": null,
        "auto_import_id": null,
        "availability": "anytime",
        "banned_at": null,
        "billing_address": null,
        "bio": "Specialist in management and business growth.",
        "call_status_id": 5,
        "call_status_name": "no-answer",
        "capital_amount_in_cents": 0,
        "children_count": 2,
        "church": "Liberty Church",
        "city_sub_district": "DOWNTOWN LOS ANGELES",
        "closed_invoices_amount_in_cents": null,
        "closed_invoices_count": null,
        "contact_status_id": 3,
        "contact_status_name": "Answered",
        "could_vote_status": 1,
        "demo": "W",
        "donations_amount_in_cents": 0,
        "donations_amount_this_cycle_in_cents": 0,
        "donations_count": 0,
        "donations_count_this_cycle": 0,
        "donations_pledged_amount_in_cents": 0,
        "donations_raised_amount_in_cents": 0,
        "donations_raised_amount_this_cycle_in_cents": 0,
        "donations_raised_count": 0,
        "donations_raised_count_this_cycle": 0,
        "donations_to_raise_amount_in_cents": 0,
        "email1": "test@example.com",
        "email1_is_bad": false,
        "email2": null,
        "email2_is_bad": false,
        "email3": null,
        "email3_is_bad": false,
        "email4": null,
        "email4_is_bad": false,
        "ethnicity": null,
        "facebook_address": null,
        "facebook_profile_url": "http://www.facebook.com/profile.php?id=124071",
        "facebook_updated_at": "2014-02-25T11:22:12-04:00",
        "facebook_username": "alice",
        "fax_number": null,
        "federal_donotcall": false,
        "first_donated_at": "2013-02-02T11:51:23-05:00",
        "first_fundraised_at": "2013-04-02T11:51:23-05:00",
        "first_invoice_at": "2013-01-02T11:51:23-05:00",
        "first_prospect_at": "2013-11-02T11:51:23-05:00",
        "first_recruited_at": "2013-05-02T11:51:23-05:00",
        "first_supporter_at": "2014-02-02T11:51:23-05:00",
        "first_volunteer_at": "2013-05-02T11:51:23-05:00",
        "full_name": "Bob Smith",
        "home_address": null,
        "import_id": null,
        "inferred_party": "H",
        "inferred_support_level": 1,
        "invoice_payments_amount_in_cents": 0,
        "invoice_payments_referred_amount_in_cents": 0,
        "invoices_amount_in_cents": null,
        "invoices_count": null,
        "is_deceased": false,
        "is_donor": false,
        "is_fundraiser": false,
        "is_ignore_donation_limits": false,
        "is_leaderboardable": true,
        "is_mobile_bad": false,
        "is_possible_duplicate": false,
        "is_profile_private": false,
        "is_profile_searchable": true,
        "is_prospect": false,
        "is_supporter": true,
        "is_survey_question_private": false,
        "language": "EN",
        "last_call_id": 2378,
        "last_contacted_at": null,
        "last_contacted_by": null,
        "last_donated_at": "2014-02-02T11:51:23-05:00",
        "last_fundraised_at": "2014-01-01T11:51:23-05:00",
        "last_invoice_at": null,
        "last_rule_violation_at": null,
        "legal_name": null,
        "locale": "en",
        "mailing_address": null,
        "marital_status": "S",
        "media_market_name": null,
        "meetup_address": null,
        "membership_expires_at": null,
        "membership_level_name": null,
        "membership_started_at": null,
        "middle_name": "T.",
        "mobile_normalized": null,
        "nbec_precinct_code": null,
        "note_updated_at": "2014-01-01T11:51:23-05:00",
        "outstanding_invoices_amount_in_cents": null,
        "outstanding_invoices_count": null,
        "overdue_invoices_count": 0,
        "page_slug": null,
        "parent": null,
        "parent_id": null,
        "party_member": false,
        "phone_normalized": null,
        "phone_time": "daytime",
        "precinct_code": "9876",
        "precinct_name": "9876",
        "prefix": null,
        "previous_party": "U",
        "primary_email_id": 1,
        "priority_level": 4,
        "priority_level_changed_at": null,
        "profile_content": "I support Abraham Lincoln for President.",
        "profile_content_html": "<p>I support Abraham Lincoln for President.</p>",
        "profile_headline": "Abe is back!",
        "received_capital_amount_in_cents": 0,
        "recruiter": {
            "birthdate": "1963-02-02",
            "city_district": null,
            "civicrm_id": 9,
            "county_district": "11",
            "county_file_id": "97076395",
            "created_at": "2014-02-02T11:51:23-05:00",
            "do_not_call": false,
            "do_not_contact": false,
            "dw_id": null,
            "email": null,
            "email_opt_in": true,
            "employer": "Sun Film Foundation",
            "external_id": "781986",
            "federal_district": "0",
            "fire_district": null,
            "first_name": "Mina",
            "has_facebook": false,
            "id": 233,
            "is_twitter_follower": false,
            "is_volunteer": false,
            "judicial_district": null,
            "labour_region": null,
            "last_name": "Abbott",
            "linkedin_id": null,
            "mobile": "5738882938",
            "mobile_opt_in": true,
            "nbec_guid": "000099dc-00f0-11e2-b349-27c4eb6c1979",
            "ngp_id": null,
            "note": "Has 3 kids. Ask about the baby on the way",
            "occupation": "Community Organizer",
            "party": "P",
            "pf_strat_id": 91207702,
            "phone": "2156726335",
            "precinct_id": null,
            "primary_address": null,
            "recruiter_id": null,
            "rnc_id": 2653431,
            "rnc_regid": "003F4ED9-3C5C-4E15-8178-B84920F41BFF",
            "salesforce_id": null,
            "school_district": "Chicago Public Schools",
            "school_sub_district": null,
            "sex": "F",
            "signup_type": 0,
            "state_file_id": "100000012",
            "state_lower_district": "024",
            "state_upper_district": "1",
            "support_level": 1,
            "supranational_district": "Eastern Euro Region",
            "tags": [],
            "twitter_id": "63403772",
            "twitter_name": "AngryPig",
            "updated_at": "2014-02-02T11:51:23-05:00",
            "van_id": "2",
            "village_district": null
        },
        "recruits_count": 0,
        "registered_address": null,
        "registered_at": null,
        "religion": null,
        "rule_violations_count": 0,
        "spent_capital_amount_in_cents": 0,
        "submitted_address": "123 Main St Portland, ME 04101",
        "subnations": ["abeforprez", "operalovers"],
        "suffix": null,
        "support_level_changed_at": "2014-02-02T11:51:23-05:00",
        "support_probability_score": null,
        "turnout_probability_score": null,
        "twitter_address": null,
        "twitter_description": "Animal lover.",
        "twitter_followers_count": 564,
        "twitter_friends_count": 32,
        "twitter_location": "Dallas, TX",
        "twitter_login": "trinity",
        "twitter_updated_at": "2014-01-01T11:51:23-05:00",
        "twitter_website": "http://mytwittersite.com",
        "unsubscribed_at": null,
        "user_submitted_address": null,
        "username": null,
        "warnings_count": 0,
        "website": null,
        "work_address": null,
        "work_phone_number": null
    },
    "precinct": {
        "id": 77,
        "code": "9876",
        "name": "9876"
    }
}
```

Search Endpoint
---------------

Use this endpoint to find people that have certain attributes.

```
GET /api/v1/people/search
```

### Parameters
* `first_name` - first name search parameter
* `last_name` - last name search parameter
* `city` - city of the primary address of people to match
* `state` - state of the primary address of people to match
* `sex` - sex of the people to match (optional, M or F)
* `birthdate` - date of birth of the people to match
* `updated_since` - people updated since the given date
* `with_mobile` - only people with mobile phone numbers
* `custom_values` - match custom field values. It takes a nested format, e.g. `{"custom_values": {"my_field_slug": "abcd"}}`. In the query string this parameter would have to be encoded as `custom_values%5Bmy_field_slug%5D=abcd`.
* `civicrm_id` - civicrm_id of the person to match
* `county_file_id` - county_file_id of the person to match
* `state_file_id` - state_file_id of the person to match
* `datatrust_id` - datatrust_id of the person to match
* `dw_id` - dw_id of the person to match
* `media_market_id` - media_market_id of the person to match
* `membership_level_id` - membership_level_id of the person to match
* `ngp_id` - ngp_id of the person to match
* `pf_strat_id` - pf_strat_id of the person to match
* `van_id` - van_id of the person to match
* `salesforce_id` - salesforce_id of the person to match
* `rnc_id` - rnc_id of the person to match
* `rnc_regid` - rnc_regid of the person to match
* `external_id` - external_id of the person to match.
* `limit` - max number of results to show in one page of results (default 10, max 100).
* `__nonce` - generated pagination nonce. Do not modify.
* `__token` - generated pagination token. Do not modify.

### Example

Make the request:

```
GET https://foobar.nationbuilder.com/api/v1/people/search?first_name=Byron&city=Beverly%20Hills&state=CA
```

Should give you a response like this:

```json
{
  "next": "/api/v1/people/search?__nonce=3OUjEzI6iyybc1F3sk6YrQ&__token=ADGvBW9wM69kUiss1KqTIyVeQ5M6OwiL6ttexRFnHK9m&first_name=Byron&city=Beverly%20Hills&state=CA",
  "prev": null,
  "results": [
    {
      "birthdate": "1973-04-04",
      "city_district": "city_district_1",
      "civicrm_id": 123489,
      "county_district": "county_district_1",
      "county_file_id": "mycountyfileid",
      "created_at": "2014-02-02T11:51:23-05:00",
      "do_not_call": false,
      "do_not_contact": false,
      "dw_id": 987,
      "email": "test@example.com",
      "email_opt_in": true,
      "employer": "Texas Instruments",
      "external_id": "external",
      "federal_district": "federal_district_1",
      "fire_district": "fire_district_1",
      "first_name": "Byron",
      "has_facebook": true,
      "id": 10801,
      "is_twitter_follower": false,
      "is_volunteer": false,
      "judicial_district": "judicial_district_1",
      "labour_region": "labour_region_1",
      "last_name": "Smith",
      "linkedin_id": "linkedinid",
      "mobile": "5738882938",
      "mobile_opt_in": true,
      "nbec_guid": "c4545",
      "ngp_id": "myngpid",
      "note": "Has 3 kids. Ask about the baby on the way",
      "occupation": "Programmer",
      "party": "P",
      "pf_strat_id": 876,
      "phone": "2156726335",
      "precinct_id": 995,
      "primary_address": {
        "address1": "123 Fake St",
        "address2": null,
        "address3": null,
        "city": "Beverly Hills",
        "state": "CA",
        "country_code": "US",
        "zip": "90201",
        "lat": 34.0502,
        "lng": -117.2478
      },
      "recruiter_id": 10800,
      "rnc_id": 1234567,
      "rnc_regid": "003F4ED9-3C5C-4E15-8178-B84920F41BFF",
      "salesforce_id": "salesforceid",
      "school_district": "school_district_1",
      "school_sub_district": "school_sub_district_1",
      "sex": "F",
      "signup_type": 0,
      "state_file_id": "a12345z",
      "state_lower_district": "state_lower_district_1",
      "state_upper_district": "state_upper_district_1",
      "support_level": 1,
      "supranational_district": "region_abc",
      "tags": [],
      "twitter_id": "765",
      "twitter_name": "AngryPig",
      "updated_at": "2014-02-02T11:51:23-05:00",
      "van_id": "d6767",
      "village_district": "village_district_1"
    }
  ]
}
```

Nearby Endpoint
---------------

Use this endpoint to search for people near a location defined by latitude and longitude.

```
GET /api/v1/people/nearby
```

### Parameters
* `location` - origin of search in the format latitude,longitude (required)
* `distance` - the radius in miles for which to include results (optional, default: 1 mile)
* `limit` - max number of results to show in one page of results (default 10, max 100).
* `__nonce` - generated pagination nonce. Do not modify.
* `__token` - generated pagination token. Do not modify.

### Example

In order to search for people in the 'foobar' nation that live within a mile of Coors Field in Denver, issue a request like this:

```
GET https://foobar.nationbuilder.com/api/v1/people/nearby?location=34.0522,-118.2428&distance=1
```

You should receive a response like this:

```
{
  "next": "/api/v1/people/nearby?__nonce=3OUjEzI6iyybc1F3sk6YrQ&__token=ADGvBW9wM69kUiss1KqTIyVeQ5M6OwiL6ttexRFnHK9m&location=34.0522,-118.2428&distance=1",
  "prev": null,
  "results": [
    {
      "birthdate": "1973-04-04",
      "city_district": null,
      "civicrm_id": 7,
      "county_district": "11",
      "county_file_id": "97076395",
      "created_at": "2014-03-15T15:31:28-04:00",
      "do_not_call": false,
      "do_not_contact": false,
      "dw_id": null,
      "email": "clotilde@wisoky.org",
      "email_opt_in": true,
      "employer": "Sun Film Foundation",
      "external_id": "781986",
      "federal_district": "0",
      "fire_district": null,
      "first_name": "Gracie",
      "has_facebook": false,
      "id": 11778,
      "is_twitter_follower": false,
      "is_volunteer": false,
      "judicial_district": null,
      "labour_region": null,
      "last_name": "Leuschke",
      "linkedin_id": null,
      "mobile": "5738882938",
      "mobile_opt_in": true,
      "nbec_guid": "000099dc-00f0-11e2-b349-27c4eb6c1979",
      "ngp_id": null,
      "note": "Has 3 kids. Ask about the baby on the way",
      "occupation": "Community Organizer",
      "party": "P",
      "pf_strat_id": 91207702,
      "phone": "2156726335",
      "precinct_id": null,
      "primary_address": {
        "address1": "21292 Ahmad Rds",
        "address2": null,
        "address3": null,
        "city": "Doyleburgh",
        "state": "Wyoming",
        "country_code": "US",
        "zip": "57314-7614",
        "lat": "34.0522",
        "lng": "-118.2428"
      },
      "recruiter_id": null,
      "rnc_id": 2653431,
      "rnc_regid": "003F4ED9-3C5C-4E15-8178-B84920F41BFF",
      "salesforce_id": null,
      "school_district": "Chicago Public Schools",
      "school_sub_district": null,
      "sex": "F",
      "signup_type": 0,
      "state_file_id": "100000012",
      "state_lower_district": "024",
      "state_upper_district": "1",
      "support_level": 1,
      "supranational_district": "Eastern Euro Region",
      "tags": [],
      "twitter_id": "63403772",
      "twitter_name": "AngryPig",
      "updated_at": "2014-03-15T15:31:28-04:00",
      "van_id": "2",
      "village_district": null,
      "active_customer_expires_at": null,
      "active_customer_started_at": null,
      "author": null,
      "author_id": null,
      "auto_import_id": null,
      "availability": "anytime",
      "banned_at": null,
      "billing_address": null,
      "bio": "Specialist in management and business growth.",
      "call_status_id": 5,
      "call_status_name": "no-answer",
      "capital_amount_in_cents": 0,
      "children_count": 2,
      "church": "Liberty Church",
      "city_sub_district": "DOWNTOWN LOS ANGELES",
      "closed_invoices_amount_in_cents": null,
      "closed_invoices_count": null,
      "contact_status_id": 3,
      "contact_status_name": "Answered",
      "could_vote_status": -1,
      "demo": "W",
      "donations_amount_in_cents": 0,
      "donations_amount_this_cycle_in_cents": 0,
      "donations_count": 0,
      "donations_count_this_cycle": 0,
      "donations_pledged_amount_in_cents": 0,
      "donations_raised_amount_in_cents": 0,
      "donations_raised_amount_this_cycle_in_cents": 0,
      "donations_raised_count": 0,
      "donations_raised_count_this_cycle": 0,
      "donations_to_raise_amount_in_cents": 0,
      "email1": "clotilde@wisoky.org",
      "email1_is_bad": false,
      "email2": null,
      "email2_is_bad": false,
      "email3": null,
      "email3_is_bad": false,
      "email4": null,
      "email4_is_bad": false,
      "ethnicity": null,
      "facebook_address": null,
      "facebook_profile_url": "http://www.facebook.com/alice",
      "facebook_updated_at": "2014-02-25T11:22:12-04:00",
      "facebook_username": "alice",
      "fax_number": null,
      "federal_donotcall": false,
      "first_donated_at": "2013-02-25T11:22:12-04:00",
      "first_fundraised_at": "2013-12-15T11:22:12-04:00",
      "first_invoice_at": "2014-01-21T11:22:12-04:00",
      "first_prospect_at": "2013-10-25T11:22:12-04:00",
      "first_recruited_at": "2013-05-25T11:22:12-04:00",
      "first_supporter_at": "2014-03-15T15:31:28-04:00",
      "first_volunteer_at": "2014-01-11T11:22:12-04:00",
      "full_name": "Gracie Leuschke",
      "home_address": {
        "address1": "21292 Ahmad Rds",
        "address2": null,
        "address3": null,
        "city": "Doyleburgh",
        "state": "Wyoming",
        "country_code": "US",
        "zip": "57314-7614",
        "lat": "34.0522",
        "lng": "-118.2428"
      },
      "import_id": null,
      "inferred_party": "H",
      "inferred_support_level": 1,
      "invoice_payments_amount_in_cents": 0,
      "invoice_payments_referred_amount_in_cents": 0,
      "invoices_amount_in_cents": null,
      "invoices_count": null,
      "is_deceased": false,
      "is_donor": false,
      "is_fundraiser": false,
      "is_ignore_donation_limits": false,
      "is_leaderboardable": true,
      "is_mobile_bad": false,
      "is_possible_duplicate": false,
      "is_profile_private": false,
      "is_profile_searchable": true,
      "is_prospect": false,
      "is_supporter": true,
      "is_survey_question_private": false,
      "language": "EN",
      "last_call_id": 2378,
      "last_contacted_at": null,
      "last_contacted_by": null,
      "last_donated_at": "2014-02-02T11:51:23-05:00",
      "last_fundraised_at": "2014-01-01T11:51:23-05:00",
      "last_invoice_at": null,
      "last_rule_violation_at": null,
      "legal_name": null,
      "locale": "en",
      "mailing_address": null,
      "marital_status": "S",
      "media_market_name": null,
      "meetup_address": null,
      "membership_expires_at": null,
      "membership_level_name": null,
      "membership_started_at": null,
      "middle_name": "T.",
      "mobile_normalized": null,
      "nbec_precinct_code": null,
      "note_updated_at": "2014-01-01T11:51:23-05:00",
      "outstanding_invoices_amount_in_cents": null,
      "outstanding_invoices_count": null,
      "overdue_invoices_count": 0,
      "page_slug": null,
      "parent": null,
      "parent_id": null,
      "party_member": false,
      "phone_normalized": null,
      "phone_time": "daytime",
      "precinct_code": null,
      "precinct_name": null,
      "prefix": null,
      "previous_party": "U",
      "primary_email_id": 1,
      "priority_level": 4,
      "priority_level_changed_at": null,
      "profile_content": "I support Abraham Lincoln for President.",
      "profile_content_html": "<p>I support Abraham Lincoln for President.</p>",
      "profile_headline": "Abe is back!",
      "received_capital_amount_in_cents": 0,
      "recruiter": null,
      "recruits_count": 0,
      "registered_address": null,
      "registered_at": null,
      "religion": null,
      "rule_violations_count": 0,
      "spent_capital_amount_in_cents": 0,
      "submitted_address": "123 Main St Portland, ME 04101",
      "subnations": ["abeforprez", "operalovers"],
      "suffix": null,
      "support_level_changed_at": "2014-01-01T11:51:23-05:00",
      "support_probability_score": null,
      "turnout_probability_score": null,
      "twitter_address": null,
      "twitter_description": "Animal lover.",
      "twitter_followers_count": 564,
      "twitter_friends_count": 32,
      "twitter_location": "Dallas, TX",
      "twitter_login": "trinity",
      "twitter_updated_at": "2014-01-01T11:51:23-05:00",
      "twitter_website": "http://mytwittersite.com",
      "unsubscribed_at": null,
      "user_submitted_address": null,
      "username": null,
      "warnings_count": 0,
      "website": null,
      "work_address": null,
      "work_phone_number": null
    }
  ]
}
```

Create Endpoint
---------------

This endpoint creates a person with the provided data. It returns a full representation of the person that was created. If the creation step fails, it returns an error.

```
POST /api/v1/people
```

### Parameters

* `person` - the resource of the person to be created

A person is considered valid with a name, a phone number or an email.  If a person you create does not meet these criteria you will receive an error for a field called identity.

### Example

Make the request:

```
POST /api/v1/people
```

With attached body content like this:

```json
{
  "person": {
    "email": "bob@example.com",
    "last_name": "Smith",
    "first_name": "Bob",
    "sex": "M",
    "signup_type": 0,
    "employer": "Dexter Labs",
    "party": "P",
    "registered_address": {
      "state": "TX",
      "country_code": "US"
    }
  }
}
```
You will receive a response of status 200, with response body like this:

```json
{
  "person": {
    "birthdate": null,
    "city_district": null,
    "civicrm_id": null,
    "county_district": null,
    "county_file_id": null,
    "created_at": "2014-02-02T11:51:23-05:00",
    "do_not_call": false,
    "do_not_contact": false,
    "dw_id": null,
    "email": "bob@example.com",
    "email_opt_in": true,
    "employer": "Dexter Labs",
    "external_id": null,
    "federal_district": null,
    "fire_district": null,
    "first_name": "Bob",
    "has_facebook": false,
    "id": 9682,
    "is_twitter_follower": false,
    "is_volunteer": false,
    "judicial_district": null,
    "labour_region": null,
    "last_name": "Smith",
    "linkedin_id": null,
    "mobile": null,
    "mobile_opt_in": true,
    "nbec_guid": null,
    "ngp_id": null,
    "note": null,
    "occupation": null,
    "party": "P",
    "pf_strat_id": null,
    "phone": null,
    "precinct_id": null,
    "primary_address": {
      "address1": null,
      "address2": null,
      "address3": null,
      "city": null,
      "state": "TX",
      "country_code": "US",
      "zip": null,
      "lat": null,
      "lng": null
    },
    "recruiter_id": null,
    "rnc_id": null,
    "rnc_regid": null,
    "salesforce_id": null,
    "school_district": null,
    "school_sub_district": null,
    "sex": "M",
    "signup_type": 0,
    "state_file_id": null,
    "state_lower_district": null,
    "state_upper_district": null,
    "support_level": null,
    "supranational_district": null,
    "tags": [],
    "twitter_id": null,
    "twitter_name": null,
    "updated_at": "2014-02-02T11:51:23-05:00",
    "van_id": null,
    "village_district": null,
    "active_customer_expires_at": null,
    "active_customer_started_at": null,
    "author": null,
    "author_id": null,
    "auto_import_id": null,
    "availability": null,
    "banned_at": null,
    "billing_address": null,
    "bio": null,
    "call_status_id": null,
    "call_status_name": null,
    "capital_amount_in_cents": 0,
    "children_count": 0,
    "church": null,
    "city_sub_district": null,
    "closed_invoices_amount_in_cents": null,
    "closed_invoices_count": null,
    "contact_status_id": null,
    "contact_status_name": null,
    "could_vote_status": null,
    "demo": null,
    "donations_amount_in_cents": 0,
    "donations_amount_this_cycle_in_cents": 0,
    "donations_count": 0,
    "donations_count_this_cycle": 0,
    "donations_pledged_amount_in_cents": 0,
    "donations_raised_amount_in_cents": 0,
    "donations_raised_amount_this_cycle_in_cents": 0,
    "donations_raised_count": 0,
    "donations_raised_count_this_cycle": 0,
    "donations_to_raise_amount_in_cents": 0,
    "email1": "bob@example.com",
    "email1_is_bad": false,
    "email2": null,
    "email2_is_bad": false,
    "email3": null,
    "email3_is_bad": false,
    "email4": null,
    "email4_is_bad": false,
    "ethnicity": null,
    "facebook_address": null,
    "facebook_profile_url": null,
    "facebook_updated_at": null,
    "facebook_username": null,
    "fax_number": null,
    "federal_donotcall": false,
    "first_donated_at": null,
    "first_fundraised_at": null,
    "first_invoice_at": null,
    "first_prospect_at": null,
    "first_recruited_at": null,
    "first_supporter_at": "2014-02-02T11:51:23-05:00",
    "first_volunteer_at": null,
    "full_name": "Bob Smith",
    "home_address": null,
    "import_id": null,
    "inferred_party": null,
    "inferred_support_level": null,
    "invoice_payments_amount_in_cents": 0,
    "invoice_payments_referred_amount_in_cents": 0,
    "invoices_amount_in_cents": null,
    "invoices_count": null,
    "is_deceased": false,
    "is_donor": false,
    "is_fundraiser": false,
    "is_ignore_donation_limits": false,
    "is_leaderboardable": true,
    "is_mobile_bad": false,
    "is_possible_duplicate": false,
    "is_profile_private": false,
    "is_profile_searchable": true,
    "is_prospect": false,
    "is_supporter": true,
    "is_survey_question_private": false,
    "language": null,
    "last_call_id": null,
    "last_contacted_at": null,
    "last_contacted_by": null,
    "last_donated_at": null,
    "last_fundraised_at": null,
    "last_invoice_at": null,
    "last_rule_violation_at": null,
    "legal_name": null,
    "locale": null,
    "mailing_address": null,
    "marital_status": null,
    "media_market_name": null,
    "meetup_address": null,
    "membership_expires_at": null,
    "membership_level_name": null,
    "membership_started_at": null,
    "middle_name": null,
    "mobile_normalized": null,
    "nbec_precinct_code": null,
    "note_updated_at": null,
    "outstanding_invoices_amount_in_cents": null,
    "outstanding_invoices_count": null,
    "overdue_invoices_count": 0,
    "page_slug": null,
    "parent": null,
    "parent_id": null,
    "party_member": null,
    "phone_normalized": null,
    "phone_time": null,
    "precinct_code": null,
    "precinct_name": null,
    "prefix": null,
    "previous_party": null,
    "primary_email_id": 1,
    "priority_level": null,
    "priority_level_changed_at": null,
    "profile_content": null,
    "profile_content_html": null,
    "profile_headline": null,
    "received_capital_amount_in_cents": 0,
    "recruiter": null,
    "recruits_count": 0,
    "registered_address": {
      "address1": null,
      "address2": null,
      "address3": null,
      "city": null,
      "state": "TX",
      "country_code": "US",
      "zip": null,
      "lat": null,
      "lng": null
    },
    "registered_at": null,
    "religion": null,
    "rule_violations_count": 0,
    "spent_capital_amount_in_cents": 0,
    "submitted_address": null,
    "subnations": [],
    "suffix": null,
    "support_level_changed_at": null,
    "support_probability_score": null,
    "turnout_probability_score": null,
    "twitter_address": null,
    "twitter_description": null,
    "twitter_followers_count": null,
    "twitter_friends_count": null,
    "twitter_location": null,
    "twitter_login": null,
    "twitter_updated_at": null,
    "twitter_website": null,
    "unsubscribed_at": null,
    "user_submitted_address": null,
    "username": null,
    "warnings_count": 0,
    "website": null,
    "work_address": null,
    "work_phone_number": null
  },
  "precinct": null
}
```

Update Endpoint
---------------

This endpoint updates a person with the provided id to have the provided data.  It returns a full representation of the updated person.  If the update step fails, it returns an error.

```
PUT /api/v1/people/:id
```

### Parameters

* `person` - the resource attributes of the person to change

### Example

Make this request (assuming you have a person with id 54):

```
PUT /api/v1/people/54
```

With request body like this:

```json
{
  "person": {
    "first_name": "Joe",
    "email": "johndoe@gmail.com",
    "phone": "303-555-0841"
  }
}
```

You will receive a response of status 201, with response body like this:

```json
{
  "person": {
    "birthdate": "1973-04-04",
    "city_district": "city_district_1",
    "civicrm_id": 123489,
    "county_district": "county_district_1",
    "county_file_id": "mycountyfileid",
    "created_at": "2014-02-02T11:51:23-05:00",
    "do_not_call": false,
    "do_not_contact": false,
    "dw_id": 987,
    "email": "johndoe@gmail.com",
    "email_opt_in": true,
    "employer": "Texas Instruments",
    "external_id": "external",
    "federal_district": "federal_district_1",
    "fire_district": "fire_district_1",
    "first_name": "Joe",
    "has_facebook": true,
    "id": 54,
    "is_twitter_follower": false,
    "is_volunteer": false,
    "judicial_district": "judicial_district_1",
    "labour_region": "labour_region_1",
    "last_name": "Smith",
    "linkedin_id": "linkedinid",
    "mobile": "213 3944 624",
    "mobile_opt_in": true,
    "nbec_guid": "c4545",
    "ngp_id": "myngpid",
    "note": "Has 3 kids. Ask about the baby on the way",
    "occupation": "Programmer",
    "party": "D",
    "pf_strat_id": 876,
    "phone": "303-555-0841",
    "precinct_id": 55,
    "primary_address": null,
    "recruiter_id": 89,
    "rnc_id": 1234567,
    "rnc_regid": "003F4ED9-3C5C-4E15-8178-B84920F41BFF",
    "salesforce_id": "salesforceid",
    "school_district": "school_district_1",
    "school_sub_district": "school_sub_district_1",
    "sex": "F",
    "signup_type": 0,
    "state_file_id": "a12345z",
    "state_lower_district": "state_lower_district_1",
    "state_upper_district": "state_upper_district_1",
    "support_level": 1,
    "supranational_district": "region_abc",
    "tags": [],
    "twitter_id": "765",
    "twitter_name": "AngryPig",
    "updated_at": "2014-02-02T11:51:23-05:00",
    "van_id": "d6767",
    "village_district": "village_district_1",
    "active_customer_expires_at": null,
    "active_customer_started_at": null,
    "author": null,
    "author_id": null,
    "auto_import_id": null,
    "availability": "anytime",
    "banned_at": null,
    "billing_address": null,
    "bio": "Specialist in management and business growth.",
    "call_status_id": 5,
    "call_status_name": "no-answer",
    "capital_amount_in_cents": 0,
    "children_count": 2,
    "church": "Liberty Church",
    "city_sub_district": "DOWNTOWN LOS ANGELES",
    "closed_invoices_amount_in_cents": null,
    "closed_invoices_count": null,
    "contact_status_id": 3,
    "contact_status_name": "Answered",
    "could_vote_status": 1,
    "demo": "W",
    "donations_amount_in_cents": 0,
    "donations_amount_this_cycle_in_cents": 0,
    "donations_count": 0,
    "donations_count_this_cycle": 0,
    "donations_pledged_amount_in_cents": 0,
    "donations_raised_amount_in_cents": 0,
    "donations_raised_amount_this_cycle_in_cents": 0,
    "donations_raised_count": 0,
    "donations_raised_count_this_cycle": 0,
    "donations_to_raise_amount_in_cents": 0,
    "email1": "johndoe@gmail.com",
    "email1_is_bad": false,
    "email2": null,
    "email2_is_bad": false,
    "email3": null,
    "email3_is_bad": false,
    "email4": null,
    "email4_is_bad": false,
    "ethnicity": null,
    "facebook_address": null,
    "facebook_profile_url": "http://www.facebook.com/profile.php?id=124071",
    "facebook_updated_at": "2014-02-25T11:22:12-04:00",
    "facebook_username": "alice",
    "fax_number": null,
    "federal_donotcall": false,
    "first_donated_at": "2013-02-02T11:51:23-05:00",
    "first_fundraised_at": "2013-04-02T11:51:23-05:00",
    "first_invoice_at": "2013-01-02T11:51:23-05:00",
    "first_prospect_at": "2013-11-02T11:51:23-05:00",
    "first_recruited_at": "2013-05-02T11:51:23-05:00",
    "first_supporter_at": "2014-02-02T11:51:23-05:00",
    "first_volunteer_at": "2013-05-02T11:51:23-05:00",
    "full_name": "Joe Smith",
    "home_address": null,
    "import_id": null,
    "inferred_party": "H",
    "inferred_support_level": 1,
    "invoice_payments_amount_in_cents": 0,
    "invoice_payments_referred_amount_in_cents": 0,
    "invoices_amount_in_cents": null,
    "invoices_count": null,
    "is_deceased": false,
    "is_donor": false,
    "is_fundraiser": false,
    "is_ignore_donation_limits": false,
    "is_leaderboardable": true,
    "is_mobile_bad": false,
    "is_possible_duplicate": false,
    "is_profile_private": false,
    "is_profile_searchable": true,
    "is_prospect": false,
    "is_supporter": true,
    "is_survey_question_private": false,
    "language": "EN",
    "last_call_id": 2378,
    "last_contacted_at": null,
    "last_contacted_by": null,
    "last_donated_at": "2014-02-02T11:51:23-05:00",
    "last_fundraised_at": "2014-01-01T11:51:23-05:00",
    "last_invoice_at": null,
    "last_rule_violation_at": null,
    "legal_name": null,
    "locale": "en",
    "mailing_address": null,
    "marital_status": "S",
    "media_market_name": null,
    "meetup_address": null,
    "membership_expires_at": null,
    "membership_level_name": null,
    "membership_started_at": null,
    "middle_name": "T.",
    "mobile_normalized": "2133944624",
    "nbec_precinct_code": null,
    "note_updated_at": "2014-01-01T11:51:23-05:00",
    "outstanding_invoices_amount_in_cents": null,
    "outstanding_invoices_count": null,
    "overdue_invoices_count": 0,
    "page_slug": null,
    "parent": null,
    "parent_id": null,
    "party_member": false,
    "phone_normalized": "3035550841",
    "phone_time": "daytime",
    "precinct_code": "9876",
    "precinct_name": "9876",
    "prefix": null,
    "previous_party": "U",
    "primary_email_id": 1,
    "priority_level": 4,
    "priority_level_changed_at": null,
    "profile_content": "I support Abraham Lincoln for President.",
    "profile_content_html": "<p>I support Abraham Lincoln for President.</p>",
    "profile_headline": "Abe is back!",
    "received_capital_amount_in_cents": 0,
    "recruiter": {
      "birthdate": "1973-04-04",
      "city_district": null,
      "civicrm_id": 7,
      "county_district": "11",
      "county_file_id": "97076395",
      "created_at": "2014-02-02T11:51:23-05:00",
      "do_not_call": false,
      "do_not_contact": false,
      "dw_id": null,
      "email": null,
      "email_opt_in": true,
      "employer": "Sun Film Foundation",
      "external_id": "781986",
      "federal_district": "0",
      "fire_district": null,
      "first_name": "Mina",
      "has_facebook": false,
      "id": 89,
      "is_twitter_follower": false,
      "is_volunteer": false,
      "judicial_district": null,
      "labour_region": null,
      "last_name": "Abbott",
      "linkedin_id": null,
      "mobile": "5738882938",
      "mobile_opt_in": true,
      "nbec_guid": "000099dc-00f0-11e2-b349-27c4eb6c1979",
      "ngp_id": null,
      "note": "Has 3 kids. Ask about the baby on the way",
      "occupation": "Community Organizer",
      "party": "P",
      "pf_strat_id": 91207702,
      "phone": "2156726335",
      "precinct_id": null,
      "primary_address": null,
      "recruiter_id": null,
      "rnc_id": 2653431,
      "rnc_regid": "003F4ED9-3C5C-4E15-8178-B84920F41BFF",
      "salesforce_id": null,
      "school_district": "Chicago Public Schools",
      "school_sub_district": null,
      "sex": "F",
      "signup_type": 0,
      "state_file_id": "100000012",
      "state_lower_district": "024",
      "state_upper_district": "1",
      "support_level": 1,
      "supranational_district": "Eastern Euro Region",
      "tags": [],
      "twitter_id": "63403772",
      "twitter_name": "AngryPig",
      "updated_at": "2014-02-02T11:51:23-05:00",
      "van_id": "2",
      "village_district": null
    },
    "recruits_count": 0,
    "registered_address": null,
    "registered_at": null,
    "religion": null,
    "rule_violations_count": 0,
    "spent_capital_amount_in_cents": 0,
    "submitted_address": "123 Main St Portland, ME 04101",
    "subnations": ["abeforprez", "operalovers"],
    "suffix": null,
    "support_level_changed_at": "2014-02-02T11:51:23-05:00",
    "support_probability_score": null,
    "turnout_probability_score": null,
    "twitter_address": null,
    "twitter_description": "Animal lover.",
    "twitter_followers_count": 564,
    "twitter_friends_count": 32,
    "twitter_location": "Dallas, TX",
    "twitter_login": "trinity",
    "twitter_updated_at": "2014-01-01T11:51:23-05:00",
    "twitter_website": "http://mytwittersite.com",
    "unsubscribed_at": null,
    "user_submitted_address": null,
    "username": null,
    "warnings_count": 0,
    "website": null,
    "work_address": null,
    "work_phone_number": null
  },
  "precinct": {
      "id": 55,
      "code": "9876",
      "name": "9876"
  }
}
```

Push Endpoint
-------------

This endpoint attempts to match the input person resource to a person already in the nation. If a match is found,
the matched person is updated and a 200 status code is returned. If a match is not found, a new person is
created and a 201 status code is returned. Matches are found by including one of the following IDs in the request:

* `civicrm_id`
* `county_file_id`
* `dw_id`
* `external_id`
* `email`
* `facebook_username`
* `ngp_id`
* `salesforce_id`
* `twitter_login`
* `van_id`

```
PUT /api/v1/people/push
```

### Update Example
Assuming there is a person with the email address "byron@foobarsoftwares.com" in the foobar nation, this request:

```
PUT https://foobar.nationbuilder.com/api/v1/people/push
```

With this attached request body:

```json
{
  "person": {
    "email": "byron@foobarsoftwares.com",
    "last_name": "Erastos",
    "sex": "M"
  }
}
```

Should update the existing record to have the new name and sex, return status code 200, and this body:

```json
{
  "person": {
    "birthdate": "1973-04-04",
    "city_district": null,
    "civicrm_id": 7,
    "county_district": "11",
    "county_file_id": "97076395",
    "created_at": "2014-02-02T11:51:23-05:00",
    "do_not_call": false,
    "do_not_contact": false,
    "dw_id": null,
    "email": "byron@foobarsoftwares.com",
    "email_opt_in": true,
    "employer": "Sun Film Foundation",
    "external_id": "781986",
    "federal_district": "0",
    "fire_district": null,
    "first_name": "Byron",
    "has_facebook": false,
    "id": 9232,
    "is_twitter_follower": false,
    "is_volunteer": false,
    "judicial_district": null,
    "labour_region": null,
    "last_name": "Erastos",
    "linkedin_id": null,
    "mobile": "5738882938",
    "mobile_opt_in": true,
    "nbec_guid": "000099dc-00f0-11e2-b349-27c4eb6c1979",
    "ngp_id": null,
    "note": "Has 3 kids. Ask about the baby on the way",
    "occupation": "Community Organizer",
    "party": "P",
    "pf_strat_id": 91207702,
    "phone": "2156726335",
    "precinct_id": null,
    "primary_address": null,
    "recruiter_id": null,
    "rnc_id": 2653431,
    "rnc_regid": "003F4ED9-3C5C-4E15-8178-B84920F41BFF",
    "salesforce_id": null,
    "school_district": "Chicago Public Schools",
    "school_sub_district": null,
    "sex": "M",
    "signup_type": 0,
    "state_file_id": "100000012",
    "state_lower_district": "024",
    "state_upper_district": "1",
    "support_level": 1,
    "supranational_district": "Eastern Euro Region",
    "tags": [],
    "twitter_id": "63403772",
    "twitter_name": "AngryPig",
    "updated_at": "2014-02-02T11:51:23-05:00",
    "van_id": "2",
    "village_district": null,
    "active_customer_expires_at": null,
    "active_customer_started_at": null,
    "author": null,
    "author_id": null,
    "auto_import_id": null,
    "availability": "anytime",
    "banned_at": null,
    "billing_address": null,
    "bio": "Specialist in management and business growth.",
    "call_status_id": 5,
    "call_status_name": "no-answer",
    "capital_amount_in_cents": 0,
    "children_count": 2,
    "church": "Liberty Church",
    "city_sub_district": "DOWNTOWN LOS ANGELES",
    "closed_invoices_amount_in_cents": null,
    "closed_invoices_count": null,
    "contact_status_id": 3,
    "contact_status_name": "Answered",
    "could_vote_status": -1,
    "demo": "W",
    "donations_amount_in_cents": 0,
    "donations_amount_this_cycle_in_cents": 0,
    "donations_count": 0,
    "donations_count_this_cycle": 0,
    "donations_pledged_amount_in_cents": 0,
    "donations_raised_amount_in_cents": 0,
    "donations_raised_amount_this_cycle_in_cents": 0,
    "donations_raised_count": 0,
    "donations_raised_count_this_cycle": 0,
    "donations_to_raise_amount_in_cents": 0,
    "email1": "byron@foobarsoftwares.com",
    "email1_is_bad": false,
    "email2": null,
    "email2_is_bad": false,
    "email3": null,
    "email3_is_bad": false,
    "email4": null,
    "email4_is_bad": false,
    "ethnicity": null,
    "facebook_address": null,
    "facebook_profile_url": "http://www.facebook.com/alice",
    "facebook_updated_at": "2014-02-25T11:22:12-04:00",
    "facebook_username": "alice",
    "fax_number": null,
    "federal_donotcall": false,
    "first_donated_at": "2013-02-02T11:51:23-05:00",
    "first_fundraised_at": "2013-04-02T11:51:23-05:00",
    "first_invoice_at": "2013-01-02T11:51:23-05:00",
    "first_prospect_at": "2013-11-02T11:51:23-05:00",
    "first_recruited_at": "2013-05-02T11:51:23-05:00",
    "first_supporter_at": "2014-02-02T11:51:23-05:00",
    "first_volunteer_at": "2013-05-02T11:51:23-05:00",
    "full_name": "Byron Erastos",
    "home_address": null,
    "import_id": null,
    "inferred_party": "H",
    "inferred_support_level": 1,
    "invoice_payments_amount_in_cents": 0,
    "invoice_payments_referred_amount_in_cents": 0,
    "invoices_amount_in_cents": null,
    "invoices_count": null,
    "is_deceased": false,
    "is_donor": false,
    "is_fundraiser": false,
    "is_ignore_donation_limits": false,
    "is_leaderboardable": true,
    "is_mobile_bad": false,
    "is_possible_duplicate": false,
    "is_profile_private": false,
    "is_profile_searchable": true,
    "is_prospect": false,
    "is_supporter": true,
    "is_survey_question_private": false,
    "language": "EN",
    "last_call_id": 2378,
    "last_contacted_at": null,
    "last_contacted_by": null,
    "last_donated_at": "2014-02-02T11:51:23-05:00",
    "last_fundraised_at": "2014-01-01T11:51:23-05:00",
    "last_invoice_at": null,
    "last_rule_violation_at": null,
    "legal_name": null,
    "locale": "en",
    "mailing_address": null,
    "marital_status": "S",
    "media_market_name": null,
    "meetup_address": null,
    "membership_expires_at": null,
    "membership_level_name": null,
    "membership_started_at": null,
    "middle_name": "T.",
    "mobile_normalized": null,
    "nbec_precinct_code": null,
    "note_updated_at": "2014-01-01T11:51:23-05:00",
    "outstanding_invoices_amount_in_cents": null,
    "outstanding_invoices_count": null,
    "overdue_invoices_count": 0,
    "page_slug": null,
    "parent": null,
    "parent_id": null,
    "party_member": false,
    "phone_normalized": null,
    "phone_time": "daytime",
    "precinct_code": null,
    "precinct_name": null,
    "prefix": null,
    "previous_party": "U",
    "primary_email_id": 1,
    "priority_level": 4,
    "priority_level_changed_at": null,
    "profile_content": "I support Abraham Lincoln for President.",
    "profile_content_html": "<p>I support Abraham Lincoln for President.</p>",
    "profile_headline": "Abe is back!",
    "received_capital_amount_in_cents": 0,
    "recruiter": null,
    "recruits_count": 0,
    "registered_address": null,
    "registered_at": null,
    "religion": null,
    "rule_violations_count": 0,
    "spent_capital_amount_in_cents": 0,
    "submitted_address": "123 Main St Portland, ME 04101",
    "subnations": ["abeforprez", "operalovers"],
    "suffix": null,
    "support_level_changed_at": "2014-01-01T11:51:23-05:00",
    "support_probability_score": null,
    "turnout_probability_score": null,
    "twitter_address": null,
    "twitter_description": "Animal lover.",
    "twitter_followers_count": 564,
    "twitter_friends_count": 32,
    "twitter_location": "Dallas, TX",
    "twitter_login": "trinity",
    "twitter_updated_at": "2014-01-01T11:51:23-05:00",
    "twitter_website": "http://mytwittersite.com",
    "unsubscribed_at": null,
    "user_submitted_address": null,
    "username": null,
    "warnings_count": 0,
    "website": null,
    "work_address": null,
    "work_phone_number": null
  },
  "precinct": null
}
```

### Creation example
Assuming there is no matching person in the foobar nation, make the request:

```
PUT https://foobar.nationbuilder.com/api/v1/people/push
```

With this attached request body:

```json
{
  "person": {
    "email": "byron@foobarsoftwares.com",
    "first_name": "Byron",
    "last_name": "Erastos",
    "sex": "M"
  }
}
```

A new record will be created with the provided attributes and you will receive a response of status 201, with response body like this:

```json
{
  "person": {
    "birthdate": null,
    "city_district": null,
    "civicrm_id": null,
    "county_district": null,
    "county_file_id": null,
    "created_at": "2014-02-02T11:51:23-05:00",
    "do_not_call": false,
    "do_not_contact": false,
    "dw_id": null,
    "email": "byron@foobarsoftwares.com",
    "email_opt_in": true,
    "employer": null,
    "external_id": null,
    "federal_district": null,
    "fire_district": null,
    "first_name": "Byron",
    "has_facebook": false,
    "id": 9232,
    "is_twitter_follower": false,
    "is_volunteer": false,
    "judicial_district": null,
    "labour_region": null,
    "last_name": "Erastos",
    "linkedin_id": null,
    "mobile": null,
    "mobile_opt_in": true,
    "nbec_guid": null,
    "ngp_id": null,
    "note": null,
    "occupation": null,
    "party": null,
    "pf_strat_id": null,
    "phone": null,
    "precinct_id": null,
    "primary_address": null,
    "recruiter_id": null,
    "rnc_id": null,
    "rnc_regid": null,
    "salesforce_id": null,
    "school_district": null,
    "school_sub_district": null,
    "sex": "M",
    "signup_type": 0,
    "state_file_id": null,
    "state_lower_district": null,
    "state_upper_district": null,
    "support_level": null,
    "supranational_district": null,
    "tags": [],
    "twitter_id": null,
    "twitter_name": null,
    "updated_at": "2014-02-02T11:51:23-05:00",
    "van_id": null,
    "village_district": null,
    "active_customer_expires_at": null,
    "active_customer_started_at": null,
    "author": null,
    "author_id": null,
    "auto_import_id": null,
    "availability": null,
    "banned_at": null,
    "billing_address": null,
    "bio": null,
    "call_status_id": null,
    "call_status_name": null,
    "capital_amount_in_cents": 0,
    "children_count": 0,
    "church": null,
    "city_sub_district": null,
    "closed_invoices_amount_in_cents": null,
    "closed_invoices_count": null,
    "contact_status_id": null,
    "contact_status_name": null,
    "could_vote_status": null,
    "demo": null,
    "donations_amount_in_cents": 0,
    "donations_amount_this_cycle_in_cents": 0,
    "donations_count": 0,
    "donations_count_this_cycle": 0,
    "donations_pledged_amount_in_cents": 0,
    "donations_raised_amount_in_cents": 0,
    "donations_raised_amount_this_cycle_in_cents": 0,
    "donations_raised_count": 0,
    "donations_raised_count_this_cycle": 0,
    "donations_to_raise_amount_in_cents": 0,
    "email1": "byron@foobarsoftwares.com",
    "email1_is_bad": false,
    "email2": null,
    "email2_is_bad": false,
    "email3": null,
    "email3_is_bad": false,
    "email4": null,
    "email4_is_bad": false,
    "ethnicity": null,
    "facebook_address": null,
    "facebook_profile_url": null,
    "facebook_updated_at": null,
    "facebook_username": null,
    "fax_number": null,
    "federal_donotcall": false,
    "first_donated_at": null,
    "first_fundraised_at": null,
    "first_invoice_at": null,
    "first_prospect_at": null,
    "first_recruited_at": null,
    "first_supporter_at": "2014-02-02T11:51:23-05:00",
    "first_volunteer_at": null,
    "full_name": "Byron Erastos",
    "home_address": null,
    "import_id": null,
    "inferred_party": null,
    "inferred_support_level": null,
    "invoice_payments_amount_in_cents": 0,
    "invoice_payments_referred_amount_in_cents": 0,
    "invoices_amount_in_cents": null,
    "invoices_count": null,
    "is_deceased": false,
    "is_donor": false,
    "is_fundraiser": false,
    "is_ignore_donation_limits": false,
    "is_leaderboardable": true,
    "is_mobile_bad": false,
    "is_possible_duplicate": false,
    "is_profile_private": false,
    "is_profile_searchable": true,
    "is_prospect": false,
    "is_supporter": true,
    "is_survey_question_private": false,
    "language": null,
    "last_call_id": null,
    "last_contacted_at": null,
    "last_contacted_by": null,
    "last_donated_at": null,
    "last_fundraised_at": null,
    "last_invoice_at": null,
    "last_rule_violation_at": null,
    "legal_name": null,
    "locale": null,
    "mailing_address": null,
    "marital_status": null,
    "media_market_name": null,
    "meetup_address": null,
    "membership_expires_at": null,
    "membership_level_name": null,
    "membership_started_at": null,
    "middle_name": null,
    "mobile_normalized": null,
    "nbec_precinct_code": null,
    "note_updated_at": null,
    "outstanding_invoices_amount_in_cents": null,
    "outstanding_invoices_count": null,
    "overdue_invoices_count": 0,
    "page_slug": null,
    "parent": null,
    "parent_id": null,
    "party_member": null,
    "phone_normalized": null,
    "phone_time": null,
    "precinct_code": null,
    "precinct_name": null,
    "prefix": null,
    "previous_party": null,
    "primary_email_id": 1,
    "priority_level": null,
    "priority_level_changed_at": null,
    "profile_content": null,
    "profile_content_html": null,
    "profile_headline": null,
    "received_capital_amount_in_cents": 0,
    "recruiter": null,
    "recruits_count": 0,
    "registered_address": null,
    "registered_at": null,
    "religion": null,
    "rule_violations_count": 0,
    "spent_capital_amount_in_cents": 0,
    "submitted_address": null,
    "subnations": [],
    "suffix": null,
    "support_level_changed_at": null,
    "support_probability_score": null,
    "turnout_probability_score": null,
    "twitter_address": null,
    "twitter_description": null,
    "twitter_followers_count": null,
    "twitter_friends_count": null,
    "twitter_location": null,
    "twitter_login": null,
    "twitter_updated_at": null,
    "twitter_website": null,
    "unsubscribed_at": null,
    "user_submitted_address": null,
    "username": null,
    "warnings_count": 0,
    "website": null,
    "work_address": null,
    "work_phone_number": null
  },
  "precinct": null
}
```

Destroy Endpoint
----------------

This endpoint removes a person with the provided id from nation.  It takes no parameters and returns response code 204 on success.

```
DELETE /api/v1/people/:id
```

Register Endpoint
-----------------

This endpoint starts a user registration process for the given person by sending an account confirmation email.

```
GET /api/v1/people/:id/register
```

### Example
Assuming a person with id 123 exists in foobar nation, make the request:

```
GET https://foobar.nationbuilder.com/api/v1/people/123/register
```

You will receive a response body like this:

```json
{
  "status": "success"
}
```

Success means that the account activation email was sent successfully.

Me Endpoint
-----------

This endpoint returns the access token's resource owner's representation.

```
GET /api/v1/people/me
```

### Example

Make the request:

```
GET https://foobar.nationbuilder.com/api/v1/people/me
```

You will receive a response of status 200 and a body like this:

```json
{
  "person": {
    "birthdate": "1973-04-04",
    "city_district": null,
    "civicrm_id": 7,
    "county_district": "11",
    "county_file_id": "97076395",
    "created_at": "2014-02-02T11:51:23-05:00",
    "do_not_call": false,
    "do_not_contact": false,
    "dw_id": null,
    "email": "clotilde@wisoky.org",
    "email_opt_in": true,
    "employer": "Sun Film Foundation",
    "external_id": "781986",
    "federal_district": "0",
    "fire_district": null,
    "first_name": "Gracie",
    "has_facebook": false,
    "id": 76,
    "is_twitter_follower": false,
    "is_volunteer": false,
    "judicial_district": null,
    "labour_region": null,
    "last_name": "Leuschke",
    "linkedin_id": null,
    "mobile": "5738882938",
    "mobile_opt_in": true,
    "nbec_guid": "000099dc-00f0-11e2-b349-27c4eb6c1979",
    "ngp_id": null,
    "note": "Has 3 kids. Ask about the baby on the way",
    "occupation": "Community Organizer",
    "party": "P",
    "pf_strat_id": 91207702,
    "phone": "2156726335",
    "precinct_id": null,
    "primary_address": null,
    "recruiter_id": null,
    "rnc_id": 2653431,
    "rnc_regid": "003F4ED9-3C5C-4E15-8178-B84920F41BFF",
    "salesforce_id": null,
    "school_district": "Chicago Public Schools",
    "school_sub_district": null,
    "sex": "F",
    "signup_type": 0,
    "state_file_id": "100000012",
    "state_lower_district": "024",
    "state_upper_district": "1",
    "support_level": 1,
    "supranational_district": "Eastern Euro Region",
    "tags": [],
    "twitter_id": "63403772",
    "twitter_name": "AngryPig",
    "updated_at": "2014-02-02T11:51:23-05:00",
    "van_id": "2",
    "village_district": null,
    "active_customer_expires_at": null,
    "active_customer_started_at": null,
    "author": null,
    "author_id": null,
    "auto_import_id": null,
    "availability": "anytime",
    "banned_at": null,
    "billing_address": null,
    "bio": "Specialist in management and business growth.",
    "call_status_id": 5,
    "call_status_name": "no-answer",
    "capital_amount_in_cents": 0,
    "children_count": 2,
    "church": "Liberty Church",
    "city_sub_district": "DOWNTOWN LOS ANGELES",
    "closed_invoices_amount_in_cents": null,
    "closed_invoices_count": null,
    "contact_status_id": 3,
    "contact_status_name": "Answered",
    "could_vote_status": -1,
    "demo": "W",
    "donations_amount_in_cents": 0,
    "donations_amount_this_cycle_in_cents": 0,
    "donations_count": 0,
    "donations_count_this_cycle": 0,
    "donations_pledged_amount_in_cents": 0,
    "donations_raised_amount_in_cents": 0,
    "donations_raised_amount_this_cycle_in_cents": 0,
    "donations_raised_count": 0,
    "donations_raised_count_this_cycle": 0,
    "donations_to_raise_amount_in_cents": 0,
    "email1": "clotilde@wisoky.org",
    "email1_is_bad": false,
    "email2": null,
    "email2_is_bad": false,
    "email3": null,
    "email3_is_bad": false,
    "email4": null,
    "email4_is_bad": false,
    "ethnicity": null,
    "facebook_address": null,
    "facebook_profile_url": "http://www.facebook.com/alice",
    "facebook_updated_at": "2014-02-25T11:22:12-04:00",
    "facebook_username": "alice",
    "fax_number": null,
    "federal_donotcall": false,
    "first_donated_at": "2013-02-02T11:51:23-05:00",
    "first_fundraised_at": "2013-04-02T11:51:23-05:00",
    "first_invoice_at": "2013-01-02T11:51:23-05:00",
    "first_prospect_at": "2013-11-02T11:51:23-05:00",
    "first_recruited_at": "2013-05-02T11:51:23-05:00",
    "first_supporter_at": "2014-02-02T11:51:23-05:00",
    "first_volunteer_at": "2013-05-02T11:51:23-05:00",
    "full_name": "Gracie Leuschke",
    "home_address": null,
    "import_id": null,
    "inferred_party": "H",
    "inferred_support_level": 1,
    "invoice_payments_amount_in_cents": 0,
    "invoice_payments_referred_amount_in_cents": 0,
    "invoices_amount_in_cents": null,
    "invoices_count": null,
    "is_deceased": false,
    "is_donor": false,
    "is_fundraiser": false,
    "is_ignore_donation_limits": false,
    "is_leaderboardable": true,
    "is_mobile_bad": false,
    "is_possible_duplicate": false,
    "is_profile_private": false,
    "is_profile_searchable": true,
    "is_prospect": false,
    "is_supporter": true,
    "is_survey_question_private": false,
    "language": "EN",
    "last_call_id": 2378,
    "last_contacted_at": null,
    "last_contacted_by": null,
    "last_donated_at": "2014-02-02T11:51:23-05:00",
    "last_fundraised_at": "2014-01-01T11:51:23-05:00",
    "last_invoice_at": null,
    "last_rule_violation_at": null,
    "legal_name": null,
    "locale": "en",
    "mailing_address": null,
    "marital_status": "S",
    "media_market_name": null,
    "meetup_address": null,
    "membership_expires_at": null,
    "membership_level_name": null,
    "membership_started_at": null,
    "middle_name": "T.",
    "mobile_normalized": null,
    "nbec_precinct_code": null,
    "note_updated_at": "2014-01-01T11:51:23-05:00",
    "outstanding_invoices_amount_in_cents": null,
    "outstanding_invoices_count": null,
    "overdue_invoices_count": 0,
    "page_slug": null,
    "parent": null,
    "parent_id": null,
    "party_member": false,
    "phone_normalized": null,
    "phone_time": "daytime",
    "precinct_code": null,
    "precinct_name": null,
    "prefix": null,
    "previous_party": "U",
    "primary_email_id": 1,
    "priority_level": 4,
    "priority_level_changed_at": null,
    "profile_content": "I support Abraham Lincoln for President.",
    "profile_content_html": "<p>I support Abraham Lincoln for President.</p>",
    "profile_headline": "Abe is back!",
    "received_capital_amount_in_cents": 0,
    "recruiter": null,
    "recruits_count": 0,
    "registered_address": null,
    "registered_at": null,
    "religion": null,
    "rule_violations_count": 0,
    "spent_capital_amount_in_cents": 0,
    "submitted_address": "123 Main St Portland, ME 04101",
    "subnations": ["abeforprez", "operalovers"],
    "suffix": null,
    "support_level_changed_at": "2014-01-01T11:51:23-05:00",
    "support_probability_score": null,
    "turnout_probability_score": null,
    "twitter_address": null,
    "twitter_description": "Animal lover.",
    "twitter_followers_count": 564,
    "twitter_friends_count": 32,
    "twitter_location": "Dallas, TX",
    "twitter_login": "trinity",
    "twitter_updated_at": "2014-01-01T11:51:23-05:00",
    "twitter_website": "http://mytwittersite.com",
    "unsubscribed_at": null,
    "user_submitted_address": null,
    "username": null,
    "warnings_count": 0,
    "website": null,
    "work_address": null,
    "work_phone_number": null
  },
  "precinct": null
}
```

Taggings
--------

This endpoint returns all tags applied to a person.

```
GET /api/v1/people/:person_id/taggings
```

Tag Person
----------

This endpoint applies one or more tags to a person.

```
PUT /api/v1/people/:person_id/taggings
```

### Example request bodies

```json
{
  "tagging": {
    "tag": "my_tag"
  }
}
```

```json
{
  "tagging": {
    "tag": ["my_tag1", "my_tag2"]
  }
}
```

Tag Removal
----------

This endpoint removes a single tag from a person.

```
DELETE /api/v1/people/:person_id/taggings/:tag_name
```

Batch Tag Removal
----------

This endpoint removes one or more tags from a person.

```
DELETE /api/v1/people/:person_id/taggings
```

### Example request bodies

```json
{
  "tagging": {
    "tag": "my_tag"
  }
}
```

```json
{
  "tagging": {
    "tag": ["my_tag1", "my_tag2"]
  }
}
```

Private Notes
-------------

Create
------

```
POST /api/v1/people/:person_id/notes
```

### Example

```json
{
  "note": {
    "content": "Seems likely to be a supporter"
  }
}
```

Custom Fields
-------------
[Custom fields](http://nationbuilder.com/custom_fields) can be set in the API, and will also be included in all person resource responses.

See documentation for [custom fields on the API](http://nationbuilder.com/custom_fields_api) for more details.


If you have suggestions for these docs, [they are public on Github and we accept pull requests](https://github.com/3dna/api_docs/blob/master/doc/people_api.md).
