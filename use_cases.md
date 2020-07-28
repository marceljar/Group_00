## Picking a Timeslot (done by Marcel)

### Actor (User)
Student with a valid account in the system and an assigned CAPSTONE group.

### Pre-conditions
Student is logged into the system. No other student from the same CAPSTONE group has already picked a timeslot for the group.

### Main Flow
1. The student clicks on the **Meetings** tab on the BTR490 website.
2. The system loads a list of meeting timeslots.
3. The students clicks on an available timeslot.
4. The system asks the student to confirm his/her choice.
5. After the student confirms his/her choice, the system reloads the page and displays that the chosen timeslot belongs to the student's group.
6. The system sends an email to all members of the group.

### Alternate Flows
- If another student from the same group has already picked a timeslot:
  1. After step 3, the system will let the student know that his/her group already has an assigned timeslot.
- If a student clicks on a timeslot that has already been picked:
  1. After step 3, the system will let the student know that the chosen timeslot is already taken. The system will allow the user to chose another timeslot, effectively sending him/her back to step 2.
- If a student does not confirm his/her choice:
  1. After step 4, the system will allow the user to chose another timeslot, effectively sending him/her back to step 2.

### Postconditions
After a student has succesfully picked a timeslot, the database gets updated with the information about which group has picked which timeslot. Moreover, each member of the group (as well as the faculty) receives an email with all information about the meeting.

---

## Sending Messages to Groups (done by Marcel)

### Actor (User)
Faculty with a valid account in the system.

### Pre-conditions
Faculty is logged into the system. Information about all groups is already stored in the database.

### Main Flow
1. The faculty clicks on the **Groups** tab on the BTR490 website.
2. The system loads a list of all groups.
3. The faculty clicks on a **send message** hyperlink below a group's list of members.
4. The system brings up a model containing a form for the faculty to enter the email's subject and contents.
5. The faculty fills up both fields.
6. The faculty clicks on a **Submit** button to send the message to all students.
7. After the system succesfuly sends the message, the modal disapears.

### Alternate Flows
- If any connection issues arise, preventing the message to be sent before it times out: 
  1. The system will add an error message to the modal, warning the faculty that the message was not sent.
- If a faculty clicks on **Close**, instead of **Submit**:
  1. The modal disappears, and no further action is taken by the system. The contents of the modal will remain, though. Allowing the faculty to pick another group to send the message, for example.

### Postconditions
After a faculty has succesfully send a message, each member of the group (as well as the faculty) receives an email with its contents.
