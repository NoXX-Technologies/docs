# Docs

Place to go for the latest changes, tips, updates related to the transition to:
- AWS and Data Pulls via Java
- Update to full Beckett Data

## Model Updates (Migrations)

create model item (generally unused for now)
id
(that's it. really just a placedholder)


migration update on cards:
- remove manufacturer_id
- remove psa_spec_id
- add item_id (foreign key constraint with item.id - see above)
- remove auto-generate on id -> its the pre-specified id (static data set)

migrate update on card_sets:
remove psa_header_id
remove psa_category
remove auto-generate on id -> its the pre-specified id (static data set)

migrate update on sports
remove auto-generate on id -> its the pre-specified id (static data set)

migrate update on manufacturer
remove auto-generate on id -> its the pre-specified id (static data set)

migrate update on set_types
remove auto-generate on id -> its the pre-specified id (static data set)

## Data Updates 
