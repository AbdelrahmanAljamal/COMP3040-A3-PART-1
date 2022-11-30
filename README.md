# Public Washrooms in Manitoba

## API Description 
  This API provides information about public washrooms in Manitoba near the user's location. The user can receive a list of information about nearby public washrooms by providing a location and specifying a maximum search radius. The user is also able to specify handicap accessible washrooms. The information submitted to the location parameter may either be the GPS coordinates of the user's device, or a postal code entered by the user. The user also can set the maximum number of washroom results returned.  
  
  The response will contain a list of information including: the location, distance, accessible conditions, and available hours of the washrooms. More information about the response can be found in the sample response section.  
  
## Endpoint(s)
  Our API is a very simple API. The only one endpoint can be hit by using a <kbd>GET</kbd> request.  
    
  <kbd>GET /washrooms</kbd> List all public washrooms near the user in Manitoba.
 
| Parameter  | Type    | Required | Description |
| :-------:  | :--:    | :------: | :---------: |
| location   | String  | Yes      | location given by user |
| radius     | int     | Yes      | search radius in meter |
| accessible | boolean | No       | handicap accessible condition of washroom |
| maxNumber  | int     | No       | maximum number of washrooms will be shown |

## Description of Resources
```
{
    ......
    
    "":
    {
        "name": "",
        "address": "",
        "postalCode": "",
        "distance": ,
        "opening": "",
        "closing": "",
        "handicap":   
    },
    
    ......

}
```
  
| Parameter   | Type    | Description |
| :------:    | :--:    | :---------: |
| name        | String  | name of the washroom (if no name, base on the building it located) |
| address     | String  | address of the washroom |
| postal code | String  | postal code of the washroom or the building |
| distance    | int     | distance between the washroom and user's location in meter |
| opening     | String  | opening time |
| closing     | String  | closing time |
| handicap    | boolean | handicap accessible condition |


## Sample Request
These are several sample requests to get information about public washrooms for a given location (by postal code) and search radius.  

<kbd>https://api.washroomhelper.org/washrooms?location="r3t2n2"&radius=500&maxNumber=10</kbd>  
or  
<kbd>https://api.washroomhelper.org/washrooms?location="r3t2n2"&radius=200</kbd>
  
Additionally, a request without parameters also can be made. This request will get a list with all public washrooms recorded among the database in Manitoba.  

<kbd>https://api.washroomhelper.org/washrooms</kbd>  

## Sample Response

```
{
    "Airport1":
    {
        "name": "Airport",
        "address": "99 port air rd.",
        "postalCode": "FLY 2HI",
        "distance": 800,
        "opening": "24/7",
        "closing": "N/A",
        "handicap": true  
    },
    
    "Airport2":
    {
        "name": "Airport",
        "address": "99 port air rd.",
        "postalCode": "FLY 2HI",
        "distance": 800,
        "opening": "24/7",
        "closing": "N/A",
        "handicap": false  
    },

    "Walmart1": 
    {
        "name": "Walmart",
        "address": "123 foo st",
        "postalCode": "ABC 123",
        "distance": 800,
        "opening": "7am",
        "closing": "11pm",
        "handicap": true  
    }
}
```









