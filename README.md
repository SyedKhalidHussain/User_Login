# User_Login
User information management system
list1 = ['syed','khalid','hussain']list2 = ['rushdi','razia','iffat']database = {}database["name"] = list1database["password"] = list2

def new_user():    name = input ("Enter a name: ")    if name in database["name"]:        print("Username already exist...")        name = input ("Enter another name: ")    password = input ("Enter a password...")    database["name"].append(name)    database["password"].append(password)
def old_user():    user = input ("Enter username and password seperated by space :")    pwd_old = user.split()[1]    name_old = user.split()[0]    try:        index = database["password"].index(pwd_old)        if ( name_old == database["name"][index] and pwd_old== database["password"][index]):            print("Welcome back",name_old)    except:        print("Incorrect Password")

def login():    option = input ("Enter the option 'N'new , 'O'old, 'E'exit: ")    if option == 'N':        new_user()    elif option == 'O':        old_user()    else:        quit()
login()
