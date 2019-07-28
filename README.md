# AzureVoting
One of the most basic threats to secure and reliable election results is Booth Capturing. It is a condemnable act, yet takes place in many major voting stations, and goes unchecked. Thus, our team's primary focus will be to provide a solution that can help end this malpractice.

##To prevent Booth Capturing in Elections
Booth Capturing can be prevented if we ensure that: 
1. The correct person casts the vote,i.e. identity of voter is confirmed.
2. The person freely and discretely casts the vote, without anyone's pressure/influence.
For our project, a combination of IoT and Azure Blockchain shall be utilized.

###Set-Up:
The **Polling Enclosure** is an enclosed space with separate  points of entry and exit, with the EVM inside and that only the voter is allowed to enter.
We assume that the voter's biometric scans(fingerprints) are available (from the Aadhar data in case of General Elections).
The EVM is linked directly to Azure Cloud, and the location wise number of votes is stored there directly for everyone to view. 
The EVM is equipped with a Fingerprint Sensor, and the Entry and Exit points of the Polling Enclosure are fitted with thermal/infrared sensors to detect the number of people entering and exiting.
The list of people who can vote at a particular booth is stored on the Azure SQL database, and is available to the public for viewing.

###Working:
st=>start: Start
op=>operation: Your Operation
cond=>condition: Yes or No?
e=>end

st->op->cond
cond(yes)->e
cond(no)->op







