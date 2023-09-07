# ISEC6000_Assignment1_Task2
 ISEC6000_Assignment1_Task2
# Task_2.  Microservices Architecture and Deployment
## Part-1. Follow the step-by-step guidelines outlined in the Saleor platform repository to effectively run a Saleor stack enriched with sample data. 
## The following steps are referenced from saleor platform's Readme file
 Step 1. Create a personal account on Github.com and proceed to fork the Saleor platform repository\
   ![4aa397aa1ff8aec9b2b156fb360051b](https://github.com/krisliuqz/isec6000-assignment1-task2/assets/54123573/d8faf5ab-f7b0-40a6-818b-bde71c37cdf0)
Step 2. Using git clone to download the repository, then using cd go to the cloned directory 
```shell
git clone https://github.com/krisliuqz/saleor-platform.git
cd saleor/platform
```
![34a593e2632f14ad87a7ba8ba5c693b](https://github.com/krisliuqz/isec6000-assignment1-task2/assets/54123573/113decd5-350b-471b-9f7c-3790748e7372)
Step 3. Build the application and then Apply Django migrations
```shell
docker compose run --rm api python3 manage.py migrate
```
![0be8fedb5cc1f9ca9e276619e74c1bb](https://github.com/krisliuqz/isec6000-assignment1-task2/assets/54123573/361a3e01-e6be-4d5e-8cbb-0a24c7d5e6cf)
Step 4. Populate the database with example data and create the admin user
```shell
docker compose run --rm api python3 manage.py populatedb --createsuperuser
```
![a19108063eeabb139721f44528b83a1](https://github.com/krisliuqz/isec6000-assignment1-task2/assets/54123573/35e01a46-68ab-4f58-b971-1ca4788f84f0)

*Note that `--createsuperuser` argument creates an admin account for `admin@example.com` with the password set to `admin`.*\
Step 5. Run the application:
```shell
docker compose up
```
![ef2e70018bb08a2ec3fb6a731008154](https://github.com/krisliuqz/isec6000-assignment1-task2/assets/54123573/1d172059-5786-4727-9655-6731d76429e8)
## Part-2. Tailor the Compose file to ensure optimal functionality:
### a. Configure the React Storefront to operate on port 3009.
### b. Assign port 9003 for the Saleor Dashboard.
### c. Initiate the stack and verify the successful launch of all services:
  ### Saleor React Storefront: Accessible at http://<Your-Linux-Server-IP>:3009.
  ### Saleor Dashboard: Reachable via http://<Your-Linux-Server-IP>:9003.
  Step 1. open docker-compose.yml and change the Saleor React Storefront port number to 3009 and Saleor Dashboard port number to 9003.
  ![4f89a0ca3e8bb0fccbc8272ee66ce24](https://github.com/krisliuqz/isec6000-assignment1-task2/assets/54123573/f609e892-4017-4a01-9a84-2a0353dc11a9)
 Step 2. Save the file and run docker compose up
 ![071730a5e2accaf613311256d479f54](https://github.com/krisliuqz/isec6000-assignment1-task2/assets/54123573/cd80cd73-e637-4a44-b8dd-de48a58c6681)
 Step 3. change the port number in the web preview to check whether the website is on
 ![image](https://github.com/krisliuqz/isec6000-assignment1-task2/assets/54123573/d4a784a1-4cc8-4b8c-a922-f3ad918b5c11)\
 Step 4. Enter localhost:9003  and localhost:3009 in URL you will see the websites
 ![image](https://github.com/krisliuqz/isec6000-assignment1-task2/assets/54123573/6f5cc21b-5d0e-4afc-91ae-ff31b579b7bb)
![e87d35bed45540b5993cdf4fe59a859](https://github.com/krisliuqz/isec6000-assignment1-task2/assets/54123573/52e3d77c-1725-45f0-aa2a-3adbe0df3cc9)
## Where is the application running?
- Saleor storefront - http://localhost:3009
- Saleor Dashboard - http://localhost:9003
## Part-3. Commit your modifications and push them to the forked repository, appending the tag isec6000-assignment1
Step 1. Using command git add to stage file for commit and commit by using git commit
```shell
git add docker-compose.yml
git commit -m"isec6000-assignment1"
```
![7a1389652442faf995256615ffd2180](https://github.com/krisliuqz/isec6000-assignment1-task2/assets/54123573/c88c3c08-eafc-41cf-939c-9d6553a9f740)
Step 2. push the commit to the main branch
![9ac02135d362398cd0ff1f781dafd7c](https://github.com/krisliuqz/isec6000-assignment1-task2/assets/54123573/d86cb1a3-8fb0-493b-ae99-f08b41d3209f)
