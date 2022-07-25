# E3/DC portal postman collection
## Content
This project contains a postman collection that allows simple/demo access to E3/DC portal data, e.g. live data and historic data. Thereby, the focus is on getting the raw data. However, the collection also includes some visulization code for pretty printing the content. Especially, for historic data, this is handy to display something human readable.

## Getting started

Start postman and create an environment with the following values, which are intentionally not included in the collection for security reasons:

| Variable name | content | required for what? |
| ------ | ------ | ------ |
| `e3dc-user`     | user name usually your email address | login to portal                            |
| `e3dc-password` | MD5 hash of your password            | login to portal (luckily hash suffices)    |
| `e3dc-serial`   | Serial number of your machine        | select the according machine in the portal |

Login by firing the requests `Authenticate` and `Select System`. Then use the other requests as per your flavor.

## Requests

| Request | Purpose | Reference to portal |
| ------ | ------ | ------ |
| `Authenticate` | Login to the portal in order to retrieve a session | Regular login screen |
| `Select System` | Select your system | Click on your system |
| `Live Data` | Get the live data | Click to display live data |
| `History` | Get historic data (default yesterday, but feel free to pimp under tab `Pre-request Script`) | Data source for the diagrams drawn in portal. Be aware that the response contains cumulated values. In the E3/DC portal there is a lot of javascript code involved to calculate the charts . |

## Contribution

Feel free to improve and enhance (especially, vistualization features) and create a pull request. No formal process involved.