## Task
Build a Django application with following functionalities
1. Exposes an API to store the emails. Feel free to use Django REST Framework
2. A view to list down the emails in the reverse chronological order and show the number of new emails added this calendar month
3. Integrate the api with the email collection widget present in this project.
3. Bonus - setup a celery task that runs every Monday and Wednesday and prints the number of new emails added in the current calendar month to the console.

 _NOTES_
 - The widget itself sits on seller's online store (3rd party site) and sends data to your app (Konigle). The API is public but we don't want anyone to misuse it.

## Steps
1. Download the attached zip file which is a git repo. The repo already contains the following
    - `widgets` - a Javascript project for creating the widget. This includes the webpack based toolchain to generate the widget's JS file. If you are not comfortable with all these, don't worry about it.
    - `static/js/e-widgets.v1.min.js` - The widget's javascript file to be included in the seller's online store. You need to configure your Django project to serve this static file to any online store.
    - `widgets/test/store.html` - A test HTML file which includes the widget. 
2. Create a Django project inside the repo.
3. Create Django app with name - unity.
4. Create a data model to store the emails.
5. Expose an REST API to be used by the widget to submit the email data.
6. Create a Django view for listing the emails. As shown in the figma file for reference : https://www.figma.com/file/CYhfwmtEK4Xm7ZsNM6Swej/Unity?node-id=0%3A1
7. Bonus - Create a celery periodic task that does what is specified above






