# FileUpload

The following project is a simple example that allows a user to upload files to an online database. It was created using Laravel 5.3, and is designed to target an Amazon S3 bucket.

This project was created by following a tutorial created by Hardik Savani, which can be accessed here: http://itsolutionstuff.com/post/laravel-5-amazon-s3-file-upload-tutorial-part-1example.html

However, I have made the following changes:

* His example requires linking to "localhost:8000/s3-image-upload" in order to access the image-upload page through a couple of reroutes. I've cut out the middle-man and made it so you can directly access the page through "localhost:8000".
* His implementation focused not only on uploading files but specifically uploading images, and had a validation step in S3ImageController.php to verify if the file was a small-enough image. I've commented out that step, allowing the upload of not only larger images but also .doc and .pdf files as well. You can uncomment said section to view the validation yourself.
* Since his implementation was focused on images, he had the image show on the page (image-upload.blade.php) on a successful upload. I've commented it out so that you don't see an unloaded image if you try to upload a non-image file. Once again, it can be uncommented.

A .env.example template has been left for you to create your own .env file. You will need your own Amazon S3 bucket to run this project. To fill the AWS fields of the .env file, do the following:

* For AWS_KEY and AWS_SECRET, go to your IAM Management Console on Amazon and create an Access Key to obtain both.
* For AWS_REGION, go to the following link and copy the Region that corresponds to bucket's Region Name: http://docs.aws.amazon.com/general/latest/gr/rande.html
* For AWS_BUCKET, simply copy your bucket's name.

Finally, once you've cloned/downloaded this repository, simply run "php artisan serve" on your Terminal or Command Line to access.
