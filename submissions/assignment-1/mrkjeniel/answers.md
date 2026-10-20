ANSWER_1: It failed because it was denided permission to read its configuraton file at /etc/course-portal/portal.conf
ANSWER_2: Its file permissions are set to -rw-------, giving out read and write access only to the owner, while the group portal and other have no access. Since course-portal belongs to the group with no access, it is denied.
ANSWER_3: 640
ANSWER_3_WHY: 400 only gives access to the owner, and 755 and 777 is openly giving access to others, which is unnecessary.
ANSWER_4_ORDER: B, G, E, D, F, A, I, C, H
ANSWER_5: Using chmod 777 grants write and execute permissions to all users on the system , allowing any unauthorized local user or process to modify, overwrite, or delete the configuration file.
ANSWER_6: (Example) The service log is no longer recording permission errors and showing successful application startup logs (.
ANSWER_7_BRIDGE: component=access control and file permissions, detect=automated log monitoring, recover=automated configuration management, proof=end-to-end HTTP health checks
