# foreverscape-captions
Caption Contest App

This project is recruitment-into-software development. The emphasis is not on particular language or technology, but building an app from scratch to learn. For ease, developer will be set up with a PHP server and a database they can add custom tables to.



<h2>Stories</h2>

<h3>Developer Stories</h3>

1) As the code-challenge developer, I want to check out this repository locally.

2) As the developer, I will create a new branch to work in (and commit and push code to).

3) I do not want to commit files to the repository containing database or server credentials (the config file), this will be added to gitignore. the ignored file will be read by the software to submit credentials. The config will also not be visible on the server.


<h3>User Stories</h3>

1) As the user, I want to go to the root URL and have it redirect to the current active contest URL.

3) As the user, I want to type in a caption immediately below the image in a text field. *bonus: it is previewed as a "comic caption" superimposed on the image as they type.

4) As the user, clicking submit should allow me to quickly login via facebook and/or google. see Facebook Developer API and Google API documentation.

5) As a user, i am required to submit my email address. The user will be presented a clear privacy policy that says we never share information (but might send updates regarding the ForeverScape that they can unsubscribe to, forever, at any time).

6) As a user, i'd like to click on a caption to upvote it. This example is not voting, but it's star rating, which is similar. Instead of averaging, we will track total rating points....
        http://code.tutsplus.com/tutorials/building-a-5-star-rating-system-with-jquery-ajax-and-php--net-11541

7) As a user the vote up and down button should be visible, but a warning is given if the user is not logged in.

8) As a user I can downvote a caption i've upvoted and vice versa, but I can never downvote twice or upvote twice for the same caption. (restricted on server).

9) As a user, i cannot perform any actions other than comment on an inactive contest.

10) As a user, I want to comment via facebook or disqus plugin.


<h3>Admin Stories</h3>

1) As an admin, I want to login with a pre-specified social media account.

2) As an admin, I want to type a page number into a input field and save that as the current contest number.
    *bonus, show the image that is entered by editing the URL string with javascript:

        ```
            <img src="'https://d2zwcujesf1bgv.cloudfront.net/prod/v13/images/tiny_preload_size/forever_' + number + '.jpg' "/>
        ```

3) As an admin, I want to save my selection to the database.

4) As an admin, I want to be able to list all email addresses/accounts for all submissions ever.

6) A URL to each contest should be unique (can just be an input field for now since we don't know the frequency), so past winners and captions pages can be deep linked.
       For example: http://contests.foreverscape.com/captions/2015/02/ where only the URL after 'captions/' is editable, i.e. the URL input field is a relative URL. 


7) As the admin, I want to be able to flag a contest as 'active' (forcing all other contests to be 'inactive'). Hint: status field on contest table in the DB.

8) As the admin, I want to be able to advertise the winner and their caption image combination on the inactive contest page.


<h2>Helpful Links</h2>

<h3>dev tools</h3>
to work on HTML files, I would suggest Submlime Text. http://www.sublimetext.com/

to work with PHP files, get Phpcs plubin for Sublime. http://neverstopbuilding.com/sublime-plugins-for-php

to work with version control, get github desktop (not my first choice). I'm not sure the best for ios.  Try this one https://www.atlassian.com/software/sourcetree/overview

<h3>learning</h3>

HTML for beginners: http://htmldog.com/guides/html/beginner/
You will notice this readme file uses HTML markup to a limited extent.

PHP for the absolute beginner: http://devzone.zend.com/6/php-101-php-for-the-absolute-beginner/

The concept of Routing describes the ability to deep link to HTML/PHP pages that "don't actually exist." Instead of building this feature from scratch, maybe a look at this comparison for a lightweight php framework to accomplish this:

 http://www.aljtmedia.com/blog/creating-a-php-rest-routing-class-for-your-application/

additionally, it allows us to hide the .php at the end of URLs without having to make a physical directory some-directory/index.php

(index.html and index.php are configured to sho up without the filename at all, in the root of a directory).
