# HTTP Request
This is how http request was made using react-native
> you can check on `api` directory 

## GET
here some example to show how we get data from backend
```
var Token = await Authentication.getItem('token')
var userid = await Authentication.getItem('user_id')
let data = {
    method: 'GET',
    headers: {
        Accept: 'application/json',
        'Content-Type': 'application/json',
        'Authorization': `Bearer ${Token}`
    },
    body: JSON.stringify(param)
}
let response = await fetch(`${apiURL}/users/${userid}`, data)
let responseJson = await response.json();
if (responseJson.response && responseJson.response == 'error') {
    return false
} else {
    return responseJson.data[0]
}
```



## POST
and this is how we post some data to backend
```
var Token = await Authentication.getItem('token')
var userid = await Authentication.getItem('user_id')
let data = {
    method: 'PATCH',
    headers: {
        Accept: 'application/json',
        'Content-Type': 'application/json',
        'Authorization': `Bearer ${Token}`
    },
    body: JSON.stringify(param)
}
let response = await fetch(`${apiURL}/users/${userid}`, data)
let responseJson = await response.json();
if (responseJson.response && responseJson.response == 'error') {
    return false
} else {
    // update user creds
    var user = await this.getUser()
    if (user.image.has_image) {
        Authentication.saveItem('name', user.name)
    }
    return true
}
```