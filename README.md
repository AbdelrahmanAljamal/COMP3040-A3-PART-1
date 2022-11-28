# Public Washrooms in Manitoba

## API Description 
  This API provides information about public washrooms in Manitoba near the user's location. The user can get a list of information about public washrooms by giving search radius (in meter) and user's location (by GPS or input postal code). A search for public washrooms will revolve around the user's location provided. The user's location can be the postal code inputed by user or the GPS information shared by user. The user also can set the number of washrooms shown in the result list.  
  
  The public waskroom information given in the response will be a list includes: the location of the public washrooms, the distance of the washrooms, accessible condition of the washrooms, and opening hours of the washrooms. More information about the response can be found in the sample response section.  
  
## Endpoint(s)
  Our API is a very simple API. The only one endpoint can be hit by using a <kbd>GET</kbd> request.  
    
  <kbd>GET /washrooms</kbd> List all public washrooms near the user in Manitoba.
 
## Parameters
| Parameter  | Type    | Required | Description |
| :-------:  | :--:    | :------: | :---------: |
| location   | String  | Yes      | location given by user |
| radius     | int     | Yes      | search radius in meter |
| accessible | boolean | No       | hadicap accessible condtion of washroom |
| maxNumber  | int     | No       | maximum number of washrooms will be shown |

## Sample Request
These are several sample requests to get information about public washrooms for a given location (by postal code) and search radius.  
<kbd>https://api.washroomhelper.org/washrooms?location="r3t2n2"&radius=500&maxNumber=10</kbd>  
or  
<kbd>https://api.washroomhelper.org/washrooms?location="r3t2n2"&radius=200</kbd>
  
Additionally, a request without parameters also can be made. This request will get a list with all public washrooms recorded among the database in Manitoba.  

<kbd>https://api.washroomhelper.org/washrooms</kbd>  

## Sample Response

## Response Object Definitions
| Parameter | Type    | Description |
| :------:  | :--:    | :---------: |
| name      | String  | name of the washroom (if no name, base on the building it located) |
| address   | String  | address of the washroom |
| code      | String  | postal code of the washroom or the building |
| distance  | int     | distance between the washroom and user's location in meter |
| opening   | String  | opening time |
| closing   | String  | closing time |
| handicap  | boolean | handicap accessible condition |








  
  
