# Find duplicate user ids on a system by parsing the /etc/passwd file

#!/usr/bin/env python
from collections import defaultdict

# Add dictionary of user ids
uids = defaultdict(list)

# loop through password file, building dictionary of uid:[usernames(list)] with open("/etc/passwd") as passwd file:
  for line in passwd: 
    lirray = line.split(":")
    uids[lirray[2]].append(lirray[0])

# loop though dictionary. 
# If duplicate usernames for uid found, print on standard out

for uid in uids:
  if len(uids[uid]) > 1:
    print ( uid + ": " + " ".join(uids[uid]))
