# LinkedInCertificationFWD
A short forwarder to get around the 255 character limit for URLs when using the LinkedIn "add to profile" certification button.

I work for an organisation that holds a public register of members.
We wanted to send each member a link so they can add their "membership" to their LinkedIn profile utilising the "filled form" model highlighted here: https://addtoprofile.linkedin.com/

Unfortunately, the amount of information we want to include in our description means the final "add to profile" URL gets very close to (or even exceeds) 255 characters.

This is a problem, as that is the maximum length that we can use as a field in MailChimp (our mailing service).

However, most of the information in each link is the same - the name of the certification, the company and the start and end date don't change that often. The important detail (their membership number - which is used to personalise the link to their entry on our register) is right at the end of the completed URL.

This code acts as a forwarder. It will accept a URL parameter (the membership number), append it to the "add to profile" code, then open the relevant form on LinkedIn, all filled out ready to use. 
