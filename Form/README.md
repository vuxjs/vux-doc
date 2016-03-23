A form component has the following props:

| name | type | description | default | example |
| -- | -- | -- | -- | -- |
| `required` | Boolean |if the form item is required | false | `<radio required></radio>` |
| `uuid` | String | element uuid | -- | -- |
| `valid` | Boolean | if value is valid | false | |
| `invalid` | Boolean | reverse of valid | true | | 
| `touched` | Boolean | whether field is touched. if field was focused, return true, else return false. | false | -- |
| `untouched` | Boolean | reverse of touched | true | -- |
| `dirty` | Boolean | whether field value was changed at least once; if so, return true, else return false. | false | -- |
| `prisine` | Boolean | reverse of dirty | true | -- |
| `errors` | Object | if invalid field exist, return error message wrapped with array, else undefined. | {} | -- |

