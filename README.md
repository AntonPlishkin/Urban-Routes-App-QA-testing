# <b>Urban-Routes-App-QA-testing</b>

The Urban Routes app is a user interface that provides transportation route selection and information on travel time and cost. Users can input their departure and destination, choose from three modes "Optimal," "Fastest," and "Custom",and select different types of transport. The application processes user input, displays routes on the map; also provides error handling for incorrect input.


## <b>Mapping at Urban Routes</b>

<b>Requirements Analysis</b>

<b>FR-4:</b> In address fields, the software shall only allow the user to enter numbers, spaces, dashes, periods, commas, and Latin characters in these fields. The maximum length of each address is 50 characters. Spaces at the beginning and end of addresses will be trimmed when the fields are not in focus. If the user enters invalid data in either field, the software shall display the error message"Incorrect address".

Check the input field “From”:
- Address field allow the user to enter “numbers”
- Address field allow the user to enter “spaces”
- Address field allow the user to enter “dashes”
- Address field allow the user to enter “periods”
- Address field allow the user to enter “commas”
- Address field allow the user to enter “Latin characters”
- Address field allow the user to enter between 1 to 50 characters
- Address field doesn’t allow the user to enter less than 1 character
- Address field doesn’t allow the user to enter more than 50 characters
- If the space at the beginning is not in focus it is cut off
- If the space at the end is not in focus it is cut off
- An “Incorrect address” error message is displayed if the the user enters invalid data

Check the input field “To”:
- Address field allow the user to enter “numbers”
- Address field allow the user to enter “spaces”
- Address field allow the user to enter “dashes”
- Address field allow the user to enter “periods”
- Address field allow the user to enter “commas”
- Address field allow the user to enter “Latin characters”
- Address field allow the user to enter between 1 to 50 characters
- Address field doesn’t allow the user to enter less than 1 character
- Address field doesn’t allow the user to enter more than 50 characters
- If the space at the beginning is not in focus it is cut off
- If the space at the end is not in focus it is cut off
- An “Incorrect address” error message is displayed if the the user enters invalid data


## <b>Carsharing at Urban Routes</b>

<b>Requirements Analysis</b>

<b>FR-CS32:</b> To order a car, the user must enter the card information and click "Add." There shall be no limit to the number of cards that can be added.

Check the field are labeled in the card details interface
- “Add card” button in the interface
- “Add card” button is always clickable

Check the field are labeled in the “Add card” interface
- “Card number” input field in the interface
- “CVV/CVC” input field in the interface
- “Add” button in the interface


<b>FR-CS33:</b> The following limits shall be applied to the input fields for card payments: 

| Field       | Limits                                                                                                                                                                       |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Card number | - Any input besides numbers is incorrect, so the system will not allow it. No more than 12 characters are allowed. The input format is: nnnn nnnn nnnn                       |
|             | - The boundary values are 0000 and 9999, inclusive.                                                                                                                          |
|             | - Spaces between numbers will be automatically added when the field is not in focus.                                                                                         |
|             | - The "Add" button will remain inactive if the input length is less than 12 characters.                                                                                      |
| CVV/CVC     | - Any input besides numbers is incorrect, so the system will not allow it. No more than 2 characters are allowed. The input format is: nn                                    |
|             | - The boundary values are 01 and 99, inclusive.                                                                                                                              |
|             | - The "Add" button will remain inactive if the input length is less than 2 characters.                                                                                       |

Check the input field “Card number”:
- Field allow the user to enter “numbers”
- Field doesn’t allow the user to enter “Letters”
- Field doesn’t allow the user to enter “Spaces”
- Field doesn’t allow the user to enter “Punctuation Marks”
- Field doesn’t allow the user to enter “Special Characters”
- Field allow the user to enter 12 characters
- Field doesn’t allow the user to enter less than 12 character
- Field doesn’t allow the user to enter more than 12 characters
- Each 4 digits allow user to enter numbers from 0000 to 9999
- Empty field doesn’t allowed
- The system automatically adds spaces between each group of 4 digits (The Input format: nnnn nnnn nnnn).
- The "Add" button is inactive if the input length is less than 12 characters.
- The "Add" button is inactive if the input length is more than 12 characters.
- The "Add" button is active if the input length is 12 characters.

Check the input field “CVV/CVC”:
- Field allow the user to enter “numbers”
- Field doesn’t allow the user to enter “Letters”
- Field doesn’t allow the user to enter “Spaces”
- Field doesn’t allow the user to enter “Punctuation Marks”
- Field doesn’t allow the user to enter “Special Characters”
- Field allow the user to enter 2 characters
- Field doesn’t allow the user to enter less than 2 character
- Field doesn’t allow the user to enter more than 2 characters
- Each 2 digits allow user to enter numbers from 01 to 99
- Each 2 digits doesn’t allow the user to enter numbers less than 01
- The "Add" button is inactive if the input length is less than 2 characters.
- The "Add" button is inactive if the input length is more than 2 characters.
- The "Add" button is active if the input length is 2 characters.


<b>FR-CS35:</b> The system shall encrypt card payment details when sending them from the client to the server.

Check the encrypt system:
- Data between client and server is transferred over secure protocols such as HTTPS
- SSL/TLS is used
- Encryption key created

Check the input field “Card number”:
- The Card number details is encrypted by Client-server by Encryption key

Check the input field “CVV/CVC”:
- CVV/CVC details is encrypted by Client-server by Encryption key
