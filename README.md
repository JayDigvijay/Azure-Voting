# AzureVoting
One of the most basic threats to secure and reliable election results is Booth Capturing. It is a condemnable act, yet takes place in many major voting stations, and goes unchecked. Thus, our team's primary focus will be to provide a solution that can help end this malpractice.

<h2>To prevent Booth Capturing in Elections</h2>
Booth Capturing can be prevented if we ensure that: 
1. The correct person casts the vote,i.e. identity of voter is confirmed.
2. The person freely and discretely casts the vote, without anyone's pressure/influence.
For our project, a combination of IoT and Azure Blockchain shall be utilized.

<h3>Set-Up:</h3>
The <strong>Polling Enclosure</strong> is an enclosed space with separate  points of entry and exit, with the EVM inside and that only the voter is allowed to enter.
We assume that the voter's biometric scans(fingerprints) are available (from the Aadhar data in case of General Elections).
The EVM is linked directly to Azure Cloud, and the location wise number of votes is stored there directly for everyone to view. 
The EVM is equipped with a Fingerprint Sensor, and the Entry and Exit points of the Polling Enclosure are fitted with thermal/infrared sensors to detect the number of people entering and exiting.
The list of people who can vote at a particular booth is stored on the Azure SQL database, and is available to the public for viewing.
A <strong>Distress</strong> Button is made available to the Poll Operator(s), as well as placed inside the Polling Enclosure

<h3>Working:</h3>
<ol>
<li> The voter shows his ID to the operator, who identifies him from that poll booth's voter list, available on the Azure database. The operator then initiates the request of transferring the voter's name from 'not-voted' to 'voted' list. This tells the EVM inside the identity of the voter, for cross-verification.</li>
<li>Upon entering the Polling Enclosure, the voter first needs to prove his identity by scanning his fingerprint on the EVM's scanner. If the fingerprint matches, the vote is registered and the voter's name is moved to the 'Voted' list.</li>
<li>The thermal sensors ensure that only one person enters the Polling Enclosure at a time. If multiple people enter, the EVM is automatically disabled till both come out, and the process must start again. If multiple people enter multiple times, a <strong>Distress Signal</strong> may be sent.</li>
<li><strong>Distress Signal:</strong> It is a signal sent to the Election Commission, as well as the local police station, denoting a possible case of BoothCapturing taking place at  any Poll Booth. The exact time of signal triggering can also be stored, along with the number of votes cast after that before police interference. The Election Commisssion may choose to make those votes invalid.</li>
</ol>

<h3>Proof-Of-Concept Implementation</h3>
The IoT part of the P.O.C. can be easily implemented on a Raspberry Pi using the appropriate sensors. The database management will be done using Azure SQL, and the whole process will be run using Azure Blockchain Services. 




