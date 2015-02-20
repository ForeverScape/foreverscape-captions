# foreverscape-captions
Caption Contest App




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

        ```html
            <img src="'https://d2zwcujesf1bgv.cloudfront.net/prod/v13/images/tiny_preload_size/forever_' + number + '.jpg' ;"/>
        ```

3) As an admin, I want to save my selection to the database.

4) As an admin, I want to be able to list all email addresses/accounts for all submissions ever.

6) A URL to each contest should be unique (can just be an input field for now since we don't know the frequency), so past winners and captions pages can be deep linked.
    ```
    For example: http://contests.foreverscape.com/captios/2015/02/
    ```

7) As the admin, I want to be able to flag a contest as 'active' (forcing all other contests to be 'inactive'). Hint: status field on contest table in the DB.

8) As the admin, I want to be able to advertise the winner and their caption image combination on the inactive contest page.
