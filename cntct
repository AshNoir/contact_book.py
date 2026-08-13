# ============================================
#              CONTACT BOOK
# ============================================
# A simple CLI-based Contact Book application.
#
# Concepts used:
# - Dictionaries
# - Nested Dictionaries
# - Functions
# - Loops
# - Conditional Statements
# - CRUD Operations
# ============================================


# --------------------------------------------
# ADD CONTACT
# --------------------------------------------
def add_name(contact_dict):

    # Ask the user for the contact's name
    name = input("Enter Name : ").strip()

    # Check whether a contact with the same name already exists
    if name in contact_dict:
        print("Contact Exists")

    else:
        # Phone number is stored as a string because
        # phone numbers are identifiers, not mathematical values.
        phone = input("Enter Phone : ").strip()

        # Ask for the email address
        mail = input("Enter Email : ").strip()

        # Create a nested dictionary for the new contact
        contact_dict[name] = {
            "Phone": phone,
            "Email": mail
        }

        print("Contact Saved Successfully!")


# --------------------------------------------
# VIEW ALL CONTACTS
# --------------------------------------------
def view_contact(contact_dict):

    print("\n========== CONTACTS ==========")

    # If the dictionary is empty, there are no contacts
    if not contact_dict:
        print("No Contacts Found.")
        return

    # Keep track of the total number of contacts
    total = 0

    # Loop through every contact
    for name in contact_dict:

        print(f"\nName : {name}")

        # Access the phone and email stored
        # inside the contact's nested dictionary
        for key, value in contact_dict[name].items():
            print(f"{key} : {value}")

        total += 1

        print("------------------------------")

    # Display total number of contacts
    print(f"Total Contacts : {total}")


# --------------------------------------------
# SEARCH CONTACT
# --------------------------------------------
def find_contact(contact_dict):

    # Ask the user which contact they want to search
    name = input("Enter Name : ").strip()

    # Check whether the name exists in the dictionary
    if name not in contact_dict:
        print("Contact Not Found.")

    else:
        # Display the selected contact's information
        print("\nContact Found!")
        print(f"Name  : {name}")
        print(f"Phone : {contact_dict[name]['Phone']}")
        print(f"Email : {contact_dict[name]['Email']}")


# --------------------------------------------
# UPDATE CONTACT
# --------------------------------------------
def contact_updt(contact_dict):

    # Ask which contact should be updated
    name = input("Enter Name : ").strip()

    # Check whether the contact exists
    if name not in contact_dict:
        print("Contact Not Found :(")

    else:
        # Display the current information
        print(f"\nCurrent Phone : {contact_dict[name]['Phone']}")
        print(f"Current Email : {contact_dict[name]['Email']}")

        # Get the new information
        newph = input("Enter New Phone : ").strip()
        newml = input("Enter New Mail : ").strip()

        # Update the existing values
        contact_dict[name]["Phone"] = newph
        contact_dict[name]["Email"] = newml

        print("Contact Updated Successfully!")


# --------------------------------------------
# DELETE CONTACT
# --------------------------------------------
def cnct_dlt(contact_dict):

    # Ask which contact should be deleted
    name = input("Enter Name : ").strip()

    # Check whether the contact exists
    if name not in contact_dict:
        print("Contact Not Found :(")

    else:
        # Ask the user for confirmation before deleting
        opt = input("Are you sure? (Y/N) : ").strip().lower()

        if opt == "n":
            print("Take Your Time, We Are Still Here :)")

        elif opt == "y":

            # Delete the selected contact
            del contact_dict[name]

            print("Contact Deleted Successfully!")

        else:
            print("Invalid Input :(")


# ============================================
#              CONTACT DATA
# ============================================

# Dictionary containing some initial contacts
cnct_dict = {
    "Rahul": {
        "Phone": "9123456780",
        "Email": "rahul@gmail.com"
    }
}


# ============================================
#                MAIN MENU
# ============================================

menu = """
================================
          CONTACT BOOK
================================

1. Add Contact
2. View All Contacts
3. Search Contact
4. Update Contact
5. Delete Contact
6. Exit
"""

print(menu)


# ============================================
#              PROGRAM LOOP
# ============================================

while True:

    # Ask the user to select an option
    choose = int(input("Choose : "))

    # Add a new contact
    if choose == 1:
        add_name(cnct_dict)

    # Display all contacts
    elif choose == 2:
        view_contact(cnct_dict)

    # Search for a contact
    elif choose == 3:
        find_contact(cnct_dict)

    # Update an existing contact
    elif choose == 4:
        contact_updt(cnct_dict)

    # Delete an existing contact
    elif choose == 5:
        cnct_dlt(cnct_dict)

    # Exit the program
    elif choose == 6:
        print("Thank you for using Contact Book!")
        break

    # Handle invalid menu options
    else:
        print("Invalid Input :(")
