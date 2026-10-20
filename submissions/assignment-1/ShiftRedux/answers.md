ANSWER_1: The course-portal service failed because it was denied permission to read /etc/course-portal/portal.conf.
ANSWER_2: The file mode is 600 (owner rw-, group ---, others ---). The owner is root, so course-portal is not the owner. It is in the course-portal group, but the group has no permissions, so it cannot read the file.
ANSWER_3: 640
ANSWER_3_WHY: 400 leaves the group with no access so the service still fails; 755 gives everyone read and execute, which is more than needed; 777 gives everyone full access, which is far too permissive.
ANSWER_4_ORDER: B, G, E, D, F, A, I, C, H
ANSWER_5: With 777, others (any user on the system) gain write and execute access, so anyone could edit or tamper with the config file and break the service.
ANSWER_6: The portal responds successfully (for example a health check returns 200) and the log shows no new "Permission denied" error after the change.
ANSWER_7_BRIDGE: component=single portal server, detect=monitoring and health-check alerts, recover=automatic failover or rollback, proof=end-to-end check that users are served
