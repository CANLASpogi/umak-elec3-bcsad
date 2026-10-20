ANSWER\_1: The course-portal service failed because it was denied permission to read /etc/course-portal/portal.conf.

ANSWER\_2: The file mode is 600 (owner rw-, group ---, others ---). The owner is root, so course-portal is not the owner. It is in the course-portal group, but the group has no permissions, so it cannot read the file.

ANSWER\_3: 640

ANSWER\_3\_WHY: 400 leaves the group with no access so the service still fails; 755 gives everyone read and execute, which is more than needed; 777 gives everyone full access, which is far too permissive.

ANSWER\_4\_ORDER: B, G, E, D, F, A, I, C, H

ANSWER\_5: With 777, any user on the system could modify the config file.

ANSWER\_6: The portal responds successfully (e.g., health check returns 200) and the log shows no new "Permission denied" error after the change.

ANSWER\_7\_BRIDGE: component=single portal server, detect=monitoring and health-check alerts, recover=automatic failover or rollback, proof=end-to-end check that users are served

