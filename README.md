# technical-req-pci-dss
PCI DSS best practices for commons environments.

## Servers
- [ ] Install or Enable the audit app into those servers.
- [ ] Create a specific user to access those servers, those keys never need to use.
- [ ] Configure those logs (messages, security, firewall, IPS/IDS and audit) to store in CloudWatch Logs.
- [ ] Those logs must have:
- User ID, Event type, Date/Hour, Status (Success or fail), Event Origin, description of data, components or items affected.
- [ ] Monitor the changes in critical files like passwd, groups, audit.conf, sshd_config, ntp.config and others.
- [ ] Enable two-factor authentication into the bastion.
- [ ] Configure into ssh a connection timeout, max 8 hours.
- [ ] Create, document and apply a Hardening baseline for servers.
- [ ] Rotate the user's password of servers and database every 90 days.
- [ ] Create a Password policy to users on the servers: 
- min: 8 char / min: 1 upper and lower char / min: 1 num char / min: 1 special char
- [ ] Block to the user doesn't use the 4 previous (min) passwords.
- [ ] Set up to user change the first password in the first access.
- [ ] Limit and block after 6 tries (in max) of wrong access for the same user.
- [ ] Set up the duration of the block to 30 minutes or until that administration enables the user.
- [ ] During connection, set up to request to type the password again every 15 minutes.
- [ ] If the connection is away, set up to request to type the password again after 15 minutes.
- [ ] Install an anti-virus into the servers and execute a scan weekly.
- [ ] Update the anti-virus into server daily.
- [ ] Apply the system update (at least the security update) monthly.
- [ ] Restrict the servers to have just one a responsibility, like web servers, mail servers and etc.
- [ ] Maintain into servers the date and hour synchronized. 

## Environment
- [ ] Create and keep update a diagram from environment topology (network side and applications).
- [ ] Create some alerts to suspects activities based on the logs (SIEM).
- [ ] Installed an IPS/IDS (squid) into the environment.
- [ ] Create and maintain an inventory from servers.
- [ ] The inventory app or list must be accessed restrict to the authorized people.
- [ ] Execute a Pentest annually in the majors URLs.
- [ ] Execute an external vulnerability scan in the majors URLs every 3 months and generate evidence.
- [ ] Review the firewall rules every 3 months and generate evidence.
- [ ] Restrict as much you can the Firewall rules to input/output traffic.
- [ ] Rotate the AWS keys every 90 days.
- [ ] Use only security connection to transfer data, like SCP, SFTP, and HTTPS.
- [ ] Each user needs to have an exclusive and confidential ID and password.
- [ ] Enable the NTP Service into servers, the AWS has an internal server to do that.
- [ ] Restrict the access to logs centralized, is good to have a group with the application logs to analyze from developers and another group to store the same log from the application and the system operational logs.
- [ ] Prioritize the solution to security issues.
- [ ] Create an assessment to contract new third-party applications, like the third-party should provide a connection over https, production, and non-production environment, they need to have at least one security certification and others.





## Miscellaneous
- [ ] Create an issue for any change into production, even to create users, release IP, the issue must be approved by a person that doesn't be involved in development or Devops.
- [ ] Don't publish internal IP or any information from the environment to not authorized person.
- [ ] Remove or change the default password from accounts or devices.
- [ ] Revoke immediately all access for an employee if he leaves the office.
- [ ] Remove all access from the inactive account in a period of 90 days.
- [ ] Forbid and avoid shared accounts or users.
- [ ] Enable MFA into all applications, servers or other components that have access to environment and data.




