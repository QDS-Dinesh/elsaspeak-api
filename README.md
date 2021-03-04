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

* **Alloted Tests**

	URL:
	* https://onlinetest.elsaspeak.com/candidates/allocatedtests.php

	Parameters to Pass:
	* token
	* keyword
	* sess (client token)

	Method:
	* POST

	Returns, if success:
	* array (of all alloted tests)
	* Sample: Array
(
    [0] => Array
        (
            [category] => Aptitude Test
            [icon] => //onlinetest.quodisys.com/images/aptitute.svg
            [topic] => Aptitude
            [maxquestions] => 0
            [totaltime] => 0
        )
    [1] => Array
        (
            [category] => English Test
            [icon] => //onlinetest.quodisys.com/images/vocabulary.svg
            [topic] => English
            [engtests] => Array
                (
                    [1] => Array
                        (
                            [topic] => Grammar
                            [maxquestions] => 40
                            [totaltime] => 30
                        )
                    [2] => Array
                        (
                            [topic] => Speaking
                            [maxquestions] => 15
                            [totaltime] => 10
                        )
                )
            [maxquestions] => 55
            [totaltime] => 40
        )
    [3] => Array
        (
            [category] => IQ Test
            [icon] => //onlinetest.quodisys.com/images/iq.svg
            [topic] => IQ
            [maxquestions] => 30
            [totaltime] => 45
        )
    [4] => Array
        (
            [category] => Technical Test
            [icon] => //onlinetest.quodisys.com/images/technical.svg
            [topic] => Technical
            [techtests] => Array
                (
                    [4] => Array
                        (
                            [topic] => Frontend
                            [maxquestions] => 15
                            [totaltime] => 30
                        )
                    [5] => Array
                        (
                            [topic] => Android
                            [maxquestions] => 15
                            [totaltime] => 30
                        )
                )
            [maxquestions] => 30
            [totaltime] => 60
        )
)

	Retuns, If fail:
	* error
