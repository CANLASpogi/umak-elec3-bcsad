ANSWER_1: The Course Materials Portal fails to start because its service account cannot read its config file /etc/course-portal/portal.conf (Permission denied).
ANSWER_2: The file is -rw------- (600): the owner root has read and write, the group course-portal has no permissions, and others have no permissions. The course-portal account is not the owner; it only matches through the course-portal group, and the group digit is 0, so it gets no read access.
ANSWER_3: 640
ANSWER_3_WHY: 400 still gives the group nothing, so course-portal still cannot read the file. 755 adds execute to a config file and lets every other user read it, which is more than needed. 777 lets every user read, write, and execute the file, which is the least safe option.
ANSWER_4_ORDER: B, G, E, D, F, A, I, C, H
ANSWER_5: Any user on the server could overwrite or tamper with portal.conf (world write), so an attacker or a mistake could change the portal's settings or break it.
ANSWER_6: The portal actually loads for a user (for example the page returns HTTP 200) and app.log shows a normal start with no new Permission denied error.
ANSWER_7_BRIDGE: component=the single application server, detect=monitoring and health checks with alerts, recover=redundant servers or automatic replacement/failover, proof=passing health checks and successful user requests
