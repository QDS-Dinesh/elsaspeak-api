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

* **Get Individual Tests**

	URL:
	* https://onlinetest.elsaspeak.com/candidates/gettests.php

	Parameters to Pass:
	* topic (like PHP, Listening, Reading, Nodejs, etc.,)

	Method:
	* POST

	Returns, if success:
	* array (of questions and answers)
	* Sample: Array
(
    [0] => Array
        (
            [question] => Small business owners ...
            [type] => radio
            [answers] => Array
                (
                    [0] => ...work hard to make their businesses grow as fast as possible.
                    [1] => ...are focused on stability, rather than growth.
                    [2] => ...aren't very good at day-to-day operations.
                )
        )
    [1] => Array
        (
            [question] => Every entrepreneur has a different ________ style.
            [type] => textbox
        )
	
	* for Listening Test, sample array:
	* Array
(
    [0] => Array
        (
            [mainquestion] => 20210120050423-listening-1.mp3
            [secondquestion] => 20210120050423-listening-2.mp3
            [type] => Audio
            [questions] => Array
                (
                    [0] => Array
                        (
                            [question] => Thanks to smartphones, people can now make ________ and efficient money transfers.
                            [type] => textbox
                        )
                    [1] => Array
                        (
                            [question] => The speaker will tell us what entrepreneurship is and will talk about vocabulary and ________ related to entrepreneurship.
                            [type] => textbox
                        )
                    [2] => Array
                        (
                            [question] => According to the audio, what is the definition of economic development?
                            [type] => radio
                            [answers] => Array
                                (
                                    [0] => The act of gaining and spending money
                                    [1] => Making sure every person has a job
                                    [2] => The process of improving the quality of people's lives
                                )
                        )

	* for Reading test, sample array:
	* Array
(
    [0] => Array
        (
            [mainquestion] => The commute time is zero. The dress code is relaxed. And, if you'd like, you can move across the country (or the world) tomorrow without having to change jobs.
There has been a meteoric rise in the number of white collar employees working from home this past year. While the COVID-19 pandemic catalyzed the shift away from the office for many companies, interest in a distributed workforce predates recent global health concerns, enabled by improving communication technology and driven by employee demands, real estate costs, and other factors. But the dramatic adoption of this radically new way of working has revealed that working from home may not be working for everyone.
[     blank 1     ]
At first glance, the benefits of working from home seem obvious for employees and employers alike. Employees are freed from sometimes arduous commutes, while employers don't need to shell out exorbitant rents for city office space. Indeed, one 2017 study found that, on average, the ability to work from home was worth an 8% decrease in salary. For their parts, employers without permanent offices to maintain are happy to spend big on annual company retreats to luxurious resorts or even provide remote employees monthly stipends for coworking space fees.
Such nontraditional work arrangements have proven to be a boon for some companies in terms of recruiting and retaining top talent, both because some employees expect the freedom that comes with working from home and because it drastically reduces — if not outright eliminates — the geographic constraints of the recruiting pool. Why limit yourself to the talent available in one city, proponents argue, when you can get the best the entire world has to offer?
Many CEOs of companies newly working from home have been tempted by these benefits and are now even considering permanently flexible work arrangements. As the feared drop in productivity associated with working from home has not materialized and workers are reluctant to return to daily commutes, company leaders are now considering the weight of these competitive advantages.
[     blank 2     ]
Unfortunately, some companies have had to make an abrupt shift to working from home and thus lacked some combination of the time, resources, and expertise to make the most out of the situation. Others are finding that while working from home presented no difficulties in the short term, working from home in the long term comes with new — perhaps insurmountable — challenges.
One of the largest hurdles companies are facing related to working from home is training new hires. While remote training capabilities have been catching up with the sudden surge in demand and importance, many leaders still say that there are a lot of gaps to fill if remote training is going to replace traditional in-peron training. Some even fear that there is no substitute for new employees sitting beside their more experienced counterparts watching how tasks are carried out and asking questions about the process. Even something as seemingly minor as company jargon, companies now realize, is not being passed onto new employees as quickly as it is in person, thus negatively affecting productivity.
"It's true that we did not see the huge drop-off in productivity that we feared immediately after the switch," one company leader said in a recent interview. "However, I don't think it's sustainable in normal circumstances. At the time, they were sent home with a laptop and no promises in the middle of a global economic crisis. Nobody wanted to be seen as ineffective in those days." 
[     blank 3     ]
Perhaps the strongest argument in favor of in-person work environments are those things that you can't schedule a video conference for. The serendipitous hallway networking meetings, the lunch conversations that reveal new perspectives on a project, and, of course, the sense that everyone is working together under one roof.
But, undeterred by tradition and convinced that working from home is more than just a trend, many offices are attempting to recreate those one-off interactions online. Some remote companies have employees video chat while on walks outside of their homes, while others set aside an hour every week for employees to chat with a co-worker they've been randomly paired with. Employee blogs, group chats, and video happy hours have also been popular strategies to build company culture while working remotely.
The efficacy of these efforts has lead to many CEOs searching for a compromise between in-person and remote working to define the future of their offices. Companies will be happy to lower their operating costs by reducing the number of employees they have to provide workspace for on any given day, and employees will be grateful for the flexibility of not having to come into the office every day. 
            [secondquestion] => 
            [type] => Text
            [questions] => Array
                (
                    [0] => Array
                        (
                            [question] => The purpose of this passage is most likely to
                            [type] => radio
                            [answers] => Array
                                (
                                    [0] => Persuade readers of the benefits of a work from home policy
                                    [1] => Inform readers of the loss of productivity that accompanies working from home
                                    [2] => Explain to readers an overview of working, including pros, cons, and strategies to cope with changes
                                    [3] => Hypothesize that working from home will continue to expand due to competition for talent
                                )
                        )

	Retuns, If fail:
	* error
