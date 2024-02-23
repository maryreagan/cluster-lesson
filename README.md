# Setting Up MongoDB Atlas Cluster
MongoDB Atlas is a fully managed cloud database service that makes it easy to set up, operate, and scale MongoDB deployments. Follow the steps below to create a MongoDB Atlas cluster:
## Step 1: Sign Up or Log In
If you don't have an account, sign up for MongoDB Atlas. If you already have an account, log in to your MongoDB Atlas account.
[MongoDB Atlas](https://cloud.mongodb.com/)
## Step 2: Create a New Cluster
After logging in, click on the Build a Cluster button.
Choose the free plan. You can also edit your provider and region
Name your cluster
Click the Create Cluster button to initiate the cluster creation process.

## Step 3: Configure Cluster Settings
Set up authentication by creating a MongoDB user with a username and password. MongoDB can autogenerate a secure password for you, make sure you copy the password for later use

In Connection Security section, MongoDB should have a listing of "My IP Address". Ensure that this is listed. If it is not listed, you can google your IP address and add it with a descriptive name. 

If you are using a VPN, you may have to add the IP address 0.0.0.0/0 , however, it is crucial to note that this setting grants access to any IP address, and as a best practice, this configuration should not be employed in production-level applications due to security considerations.

## Step 4: Connect to Your Cluster
After configuring the cluster settings, click on the Connect button again.
Choose the Connect Your Application option.
Copy the connection string provided. This string contains the necessary information to connect your application to the MongoDB Atlas cluster.

## Step 5: Connect Your Application
In Compass, we will use the same connection string to view our database. In New Connection, paste your connection string and click `Save & Connect` to get started with the lab!

### Example connection string `
`mongodb+srv://<username>:<password>@<clustername>.mongodb.net/<dbname>`

(replace `<username>`, `<password>`, and `<clustername>` with your actual credentials)

# Adding new users to your cluster after initialization

In `Database Access` under security, click `Add new database user`

Under Password Authentication, create a username and password for your new user. I like to autogenerate a secure password, copy it, and send it to them. 

From there you can edit their database privileges to your liking and when you're finished, click `Add user`

If your new user is working from a different IP address, you'll have to add their IP address which we will cover in the next steps.

# Adding an IP address after initialization

In `Network access` you can manage IP addresses that have access to your database 

To add a new IP address, click `Add IP adress`, have the new IP address ready (you can easily do this by googling your IP address) and add it into the input labeled `Access list entry`

Optionally, you can enter a name for this address in the input labeled `comment`

You can also limit the amount of time this IP adress will have access on the bottom left

Once you click `confirm`, you are all set!

