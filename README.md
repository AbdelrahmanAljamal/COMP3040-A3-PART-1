# Public Washrooms in Manitoba

## API Description 
  This API provides information about public washrooms in Manitoba near the user's location. The user can get a list of information about public washrooms by giving search radius (in meter) and user's location (by GPS or input postal code). A search for public washrooms will revolve around the user's location provided. The user's location can be the postal code inputed by user or the GPS information shared by user. The user also can set the number of washrooms shown in the result list.  
  
  The public waskroom information given in the response will be a list includes: the location of the public washrooms, the distance of the washrooms, and opening hours of the washrooms. More information about the response can be found in the sample response section.  
  
## Endpionts
  Our API is a very simple API, you only need to do a GET request to https://api.public-washrooms-Manitoba.org/json.  
  Our API is a very simple API. The only one endpoint can be hit by using a GET request.  
    
  <kbd>GET /washrooms</kbd> List all public washrooms near the user in Manitoba.
 
## Parameters
| Parameter | Type   | Required | Description |
| :-------: | :--:   | :------: | :---------: |
| location  | String | Yes      | location given by user |
| radius    | int    | Yes      | search radius in meter |
| maxNumber | int    | No       | maximum number of washrooms can be shown |

1. Location
2. Maximum search radius
3. Handicap accessible

## Sample Request
These are several sample requests to get information about public washrooms for a given location (by postal code or GPS) and search radius.  
<kbd>https://api.washroomhelper.org/washrooms?location="r3t2n2"&radius=500&maxNumber=10</kbd>  
or  
<kbd>https://api.washroomhelper.org/washrooms?location="r3t2n2"&radius=200</kbd>



  
  
