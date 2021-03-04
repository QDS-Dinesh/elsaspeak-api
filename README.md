# elsaspeak-api

* **Login**

	URL:
	* https://onlinetest.elsaspeak.com/candidates/login.php

	Parameters to Pass:
	* cl

	Method:
	* POST

	Returns, if success:
	* logo
	* keyword

	Retuns, If fail:
	* error

* **Check User**

	URL:
	* https://onlinetest.elsaspeak.com/candidates/checkuser.php

	Parameters to Pass:
	* token
	* email
	* password
	* cl
	* keyword

	Method:
	* POST

	Returns, if success:
	* msg (as Success)
	* sess (client token)

	Retuns, If fail:
	* error
