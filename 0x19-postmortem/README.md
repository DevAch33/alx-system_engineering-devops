*Issue Summary:*
- *Duration:* March 8, 2024, 10:00 AM - March 9, 2024, 2:00 AM (UTC)
- *Impact:* The API service was intermittently unavailable, causing 60% of users to experience delays and errors in data retrieval.
- *Root Cause:* A misconfigured caching layer resulted in excessive disk I/O operations, leading to resource exhaustion and service degradation.

*Timeline:*
- *March 8, 2024, 10:15 AM (UTC):* Issue detected through monitoring alerts indicating increased latency in API responses.
- *March 8, 2024, 10:30 AM (UTC):* Engineering team initiated investigation, suspecting network congestion initially.
- *March 8, 2024, 11:00 AM (UTC):* Network logs examined, ruling out congestion. Focus shifted to application-level performance.
- *March 8, 2024, 12:00 PM (UTC):* Misleading assumption made about database query optimization being the root cause, leading to unnecessary query tuning efforts.
- *March 8, 2024, 3:00 PM (UTC):* Incident escalated to senior engineering management due to prolonged service degradation.
- *March 8, 2024, 5:00 PM (UTC):* Database team involved in investigation to explore potential database performance issues.
- *March 8, 2024, 8:00 PM (UTC):* Root cause identified as misconfigured caching layer causing excessive disk I/O.
- *March 8, 2024, 9:00 PM (UTC):* Cache configuration adjusted to reduce disk I/O operations and alleviate resource strain.
- *March 9, 2024, 2:00 AM (UTC):* Service fully restored and confirmed stable.

*Root Cause and Resolution:*
- *Root Cause:* Misconfigured caching layer led to excessive disk I/O operations, exhausting system resources.
- *Resolution:* Cache configuration adjusted to optimize disk I/O usage, reducing strain on resources and improving service stability.

*Corrective and Preventative Measures:*
- *Improvements/Fixes:*
  - Review and optimize caching layer configurations across all services.
  - Implement automated monitoring for disk I/O usage to detect anomalies proactively.
  - Establish a regular audit schedule for critical system configurations to prevent similar incidents.
- *Tasks:*
  - Patch caching layer configurations to align with best practices and performance optimization guidelines.
  - Implement automated alerts for abnormal disk I/O patterns to expedite troubleshooting.
  - Schedule quarterly reviews of system configurations to ensure compliance and performance optimization.

This outage postmortem highlights the critical importance of thorough investigation and prompt escalation in diagnosing and resolving service disruptions. By addressing the root cause and implementing preventive measures, we aim to enhance system resilience and minimize the risk of similar incidents in the future.
