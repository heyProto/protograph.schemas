# ProtoGraph.TemplateDatacasts

Datacasts is the module which will store the data which is associated withe the template card. Datacasts can be created either: 

- `Manually`
  - It will be generated through forms built using json-schema of the card.
- `Automated`
  - Datacast write APIs will be exposed for people to write their own background jobs and create datacasts.
 
# Definition of Done for Template Datacasts

- We need to create clear datacast read and write APIs for usage.
- The datacast will be stored inside of `DynamoDb`
- The APIs will be made as a combination of `API Gateway` + `Aws Lambda`

- The datacasts will have the following columns
  - *Source*
  - *Data hash*
  - *latest_data* - The timestamp of the latest data from the source.
  - *last_updated_at* - The timestamp of the data last updated inside of the database 
  - *api_slug* - The external identifier. It needs to be unique.
  - *Unique Identifier*
  - *cdn_url*
  - *cdn_statistics*
  - *Data* - The actual form data which is required for the cards
  
  
- The datacast will not be updated if the data hash does not change.
- The data needs to be pushed to cdn for better availability.


# Next in line
- Search capabilities on the datacast.
- Derivative sources on the datacast.
