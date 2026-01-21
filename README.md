🔐 Securing an Amazon S3 Bucket: A Beginner-Friendly Walkthrough
Why I did this

As someone currently learning cloud computing and AWS, I wanted to practice securing storage the right way from day one. Amazon S3 is simple to use, but it’s also easy to misconfigure if you don’t understand security basics like encryption and public access control.

In this mini project, I created a secure S3 bucket, enabled encryption, and intentionally tested access to confirm that my data was protected.

🧰 What you’ll need

An AWS account

Access to the AWS Management Console

A local folder on your laptop called:
AWS-S3-Security-Screenshots

📸 I saved screenshots at every major step to document what I learned.

STEP 1: Open Amazon S3

Log into the AWS Console

Use the search bar and type S3

Click Amazon S3

You should land on the Buckets page

📸 Screenshot #1: S3 Buckets page

STEP 2: Create a new S3 bucket

Click Create bucket

Enter a globally unique bucket name

Example: fatima-s3-security-demo

Choose a region (I used the default / closest region)

Leave “Block all public access” ON (this is critical)

Click Create bucket

📸 Screenshot #2: Create bucket page with bucket name visible

STEP 3: Open the bucket

Click on the bucket you just created

You’ll see tabs like Objects, Properties, and Permissions

📸 Screenshot #3: Bucket overview with tabs visible

STEP 4: Enable encryption

Go to the Properties tab

Scroll to Default encryption

Click Edit

Enable:

Server-side encryption

Encryption type: SSE-S3

Save changes

📸 Screenshot #4: Default encryption enabled

📝 What I learned:
Encryption ensures that data is protected at rest, even if access controls are accidentally misconfigured.

STEP 5: Verify public access is blocked

Open the Permissions tab

Find Block public access

Click Edit

Make sure all checkboxes are enabled

Save changes

📸 Screenshot #5: Block public access = ON

STEP 6: Test access (security validation)

Go back to the Objects tab

Click Upload

Upload a simple .txt file

Click the uploaded file

Copy the Object URL

Open it in an incognito/private browser window

❌ You should see Access Denied

📸 Screenshot #7: Access Denied page

📝 What this confirmed:
The bucket is not publicly accessible, which means my security settings are working as intended.
