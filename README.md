# -SLA-Tracker-for-Incidents
Project: Custom SLA Tracker for Incidents

- Overview

This ServiceNow app enhances SLA visibility for Incident Management by tracking SLA health, updating incident records with visual status, and sending alerts before breaches.
Features

    Auto-tracks SLA status (On Track, Warning, Breached)

    Scheduled script evaluates SLAs every 15 minutes

    Sends warning alerts for incidents nearing breach

    Dashboard-ready field for SLA performance reports

- Technologies Used

    GlideRecord (server-side scripting)

    Scheduled Script Execution

    Task SLA (task_sla table)

    Custom Fields & UI Policies

    Notifications (optional)

    Reporting and Dashboards

- Data Model

    Incident (incident)

        Field: u_sla_status – Choice: On Track / Warning / Breached

    SLA (task_sla)

        Evaluated using planned_end_time

- How It Works

    A scheduled job runs every 15 minutes.

    For active incidents, it checks remaining SLA time.

    Based on time left:

        < 0 = Breached

        < 30 min = Warning

        Else = On Track

    Status is saved in a custom field for dashboards and alerts.

 - Screenshots

✅ Outcome

    Proactive SLA management

    Better reporting and technician visibility

    Demonstrates ServiceNow scripting and automation skills
