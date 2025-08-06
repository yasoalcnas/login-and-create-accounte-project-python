# login-and-create-accounte-project-python
#
print(50 * "=")
print("Hello")
print("My Name app {Log in and create a virtual account in google}")
print(50 * "=")
print("  ")

commend_account_full = [True, True, True, True, True]
storage_account = {
    "account_1": {
        "name": " ",
        "password": " ",
        "email": " ",
        "phone_number": " ",
        "age": " "
    },
    "account_2": {
        "name": " ",
        "password": " ",
        "email": " ",
        "phone_number": " ",
        "age": " "
    },
    "account_3": {
        "name": " ",
        "password": " ",
        "email": " ",
        "phone_number": " ",
        "age": " "
    },
    "account_4": {
        "name": " ",
        "password": " ",
        "email": " ",
        "phone_number": " ",
        "age": " "
    },
    "account_5": {
        "name": " ",
        "password": " ",
        "email": " ",
        "phone_number": " ",
        "age": " "
    }
}

# check if account is full
if storage_account["account_1"]["name"] == " ":
    commend_account_full[0] = False
if storage_account["account_1"]["name"] != " ":
    commend_account_full[0] = True

if storage_account["account_2"]["name"] == " ":
    commend_account_full[1] = False
if storage_account["account_2"]["name"] != " ":
    commend_account_full[1] = True

if storage_account["account_3"]["name"] == " ":
    commend_account_full[2] = False
if storage_account["account_3"]["name"] != " ":
    commend_account_full[2] = True

if storage_account["account_4"]["name"] == " ":
    commend_account_full[3] = False
if storage_account["account_4"]["name"] != " ":
    commend_account_full[3] = True

if storage_account["account_5"]["name"] == " ":
    commend_account_full[4] = False
if storage_account["account_5"]["name"] != " ":
    commend_account_full[4] = True


def create_account():
    global user_ask_name, user_ask_password, user_ask_email, user_ask_phone_number, user_ask_age
    user_ask_name = input("Enter your name: ")
    print("")
    user_ask_password = input("Enter your desired password: ")
    print("")
    print("name + @gmail.com")
    user_ask_email = input("Enter your desired email: ")
    print("")
    user_ask_phone_number = input("Enter your phone number: ")
    print("")
    user_ask_age = input("Enter your age: ")
    print("")
    print("Your name is: ", user_ask_name)
    print("Your password is: ", user_ask_password)
    print("Your email is: ", user_ask_email)
    print("Your phone number is: ", user_ask_phone_number)
    print("Your age is: ", user_ask_age)
    print("")
    user_ask_sure = input(
        "Are you sure you want to create this account? (yes = 1) or (no = 2): "
    )
    if user_ask_sure == "1":
        print("Account created successfully!")
        ask_create_or_login()
    if user_ask_sure == "2":
       quit()


def log_in():
    user_ask_name_login = input("Enter your name: ")
    user_ask_password_login = input("Enter your password: ")
    user_ask_email_login = input("Enter your email: ")
    user_ask_phone_number_login = input("Enter your phone number: ")
    user_ask_age_login = input("Enter your age: ")
    storage_open_my_accont = {
        "name": user_ask_name_login,
        "password": user_ask_password_login,
        "email": user_ask_email_login,
        "phone_number": user_ask_phone_number_login,
        "age": user_ask_age_login
    }
    if storage_open_my_accont == storage_account["account_1"]:
        print("The data you entered is correct.")
    if storage_open_my_accont == storage_account["account_2"]:
        print("The data you entered is correct.")
    if storage_open_my_accont == storage_account["account_3"]:
        print("The data you entered is correct.")
    if storage_open_my_accont == storage_account["account_4"]:
        print("The data you entered is correct.")
    if storage_open_my_accont == storage_account["account_5"]:
        print("The data you entered is correct.")


def ask_create_or_login():
    user_ask_request = input(
        "Do you want to (create account = 1) or (log in = 2) ?:  ")
    if user_ask_request == "1":
        create_account()
    if user_ask_request == "2":
        log_in()


def add_account_storage():
    if commend_account_full[0] == False:
        storage_account["account_1"]["name"] = user_ask_name
        storage_account["account_1"]["password"] = user_ask_password
        storage_account["account_1"]["email"] = user_ask_email
        storage_account["account_1"]["phone_number"] = user_ask_phone_number
        storage_account["account_1"]["age"] = user_ask_age
        commend_account_full[0] = True
        ask_create_or_login()
    elif commend_account_full[1] == False:
        storage_account["account_2"]["name"] = user_ask_name
        storage_account["account_2"]["password"] = user_ask_password
        storage_account["account_2"]["email"] = user_ask_email
        storage_account["account_2"]["phone_number"] = user_ask_phone_number
        storage_account["account_2"]["age"] = user_ask_age
        commend_account_full[1] = True
        ask_create_or_login()
    elif commend_account_full[2] == False:
        storage_account["account_3"]["name"] = user_ask_name
        storage_account["account_3"]["password"] = user_ask_password
        storage_account["account_3"]["email"] = user_ask_email
        storage_account["account_3"]["phone_number"] = user_ask_phone_number
        storage_account["account_3"]["age"] = user_ask_age
        commend_account_full[2] = True
        ask_create_or_login()
    elif commend_account_full[3] == False:
        storage_account["account_4"]["name"] = user_ask_name
        storage_account["account_4"]["password"] = user_ask_password
        storage_account["account_4"]["email"] = user_ask_email
        storage_account["account_4"]["phone_number"] = user_ask_phone_number
        storage_account["account_4"]["age"] = user_ask_age
        commend_account_full[3] = True
        ask_create_or_login()
    elif commend_account_full[4] == False:
        storage_account["account_5"]["name"] = user_ask_name
        storage_account["account_5"]["password"] = user_ask_password
        storage_account["account_5"]["email"] = user_ask_email
        storage_account["account_5"]["phone_number"] = user_ask_phone_number
        storage_account["account_5"]["age"] = user_ask_age
        commend_account_full[4] = True
        ask_create_or_login()
ask_create_or_login()
