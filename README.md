# s3wrapper
app for aws using node
 
Using CLI and aws s3 sync, you publish the app with your bucket name.
Then login using facebook which handles the permission for using this app.

I have used the editor in which what you see ,what you get editor ,stackoverflow used it,its
opensource ,it uses markdown so we get live preview at the bottom,i have modified to let
me select the images,this is gonna go and upload the images to s3 on my behalf.
I have actulally setup the logging the same way we set the logging-in in our terminal so 
we can see a lot of stuff (in our console) that is being sent through.originally we have dynamodb Scan to 
read all the post and sent them to user then we did our login operation to assume role.
Then we can see our putObeject operation we actually sent through.
After publish any post you can also edit and delete the post.

HTML file has some UI and its the basic skelton of the app.

In appinfo.js file we have a little basic information 
and contains all of our configuration details, we are going to use facebook
to login.Also have the region and table name there and s3 bucket name.

In app.js file most of this is controlling UI,some which is standered html DOM manipulation.
With use of sdk in line-62, we upload the assets.with the operation "s3Bucket.putObject()",this 
is very similar what we do in node-sdk.
In line-84 we also have "publishArticle()",this is our interaction with dynamodb in which we used
Item up there and we actually putItem() same way we do with node sdk.
we also have delete and some UI stuff.
In line-174 we are doing a very simple query where using response pagination to get each page.





