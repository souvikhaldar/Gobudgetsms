# Gobudgetsms

This library is used to easily make use of the Budget SMS public API to send sms, plus it lets to create message of variable length. 
## Getting Started
Just insert the details according to the example provided below and get going. No dependencies are requied to use this lib, very lightweight.


### Prerequisites

You need to have an account on Budget SMS.

### Installing

```
go get github.com/souvikhaldar/gobudgetsms
```

## Example 

Details regarding account can be found here https://www.budgetsms.net/controlpanel/api-details/
Set the credentials from your Budget SMS account, visit https://www.budgetsms.net/sms-http-api/send-sms/

```
  import (
	  "log"

	  "github.com/souvikhaldar/gobudgetsms"
  )

  func main() {
	  conf := gobudgetsms.SetConfig("username","userid","handle","customid",price,mccmnc,credit)
	  res, er := gobudgetsms.SendSMS(conf,message,"+to","from")
	  if er != nil {
		  log.Fatal(er.Error())
	  }
	  log.Print("The response after sending sms is ", res)
  }

```



## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
