# Docs

Place to go for the latest changes, tips, updates related to the transition to:
- AWS and Data Pulls via Java
- Update to full Beckett Data

## Model Updates (Migrations)

create model item (generally unused for now):
- id (that's it. really just a placedholder UUID)


migration update on cards:
- remove manufacturer_id
- remove psa_spec_id
- add item_id (foreign key constraint with item.id - see above - UUID)
- add print_run (int)
- remove auto-generate on id -> its the pre-specified id (static data set)

migrate update on card_sets:
- remove psa_header_id
- remove psa_category
- add full_name (character varying)
- add related_set_id (uuid)
- add set_blurb (character varying)
- remove auto-generate on id -> its the pre-specified id (static data set)

migrate update on sports
- remove auto-generate on id -> its the pre-specified id (static data set)
- change data type on id from UUID to int

migrate update on manufacturer
- remove auto-generate on id -> its the pre-specified id (static data set)

migrate update on set_types
- remove auto-generate on id -> its the pre-specified id (static data set)

## Data Seeding/Prep

Seeding Data Initially

Data from Heroku Production to Migrate for seeds
- Unsure about current Active Storage Images
- card_grades
- card_images
- card_sets
- card_shops
- card_values
- cards
- cards_details
- cards_players
- collection_types
- comp_sources
- comps
- conferences
- content_module_strategies
- content_modules
- countries
- details
- divisions
- grade_vendors
- grades
- interest_categories
- interest_mappings
- interests
- leagues
- manufacturers
- markets
- player_season_stats
- players
- positions
- preferences
- pricing_sites
- sale_sources
- sale_types
- set_types
- sports
- teams
- states
- whilelist_emails?
