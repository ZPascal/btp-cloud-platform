<!-- loiobbf6b336bcb84d4185429dd76dfdfaf8 -->

# Local Health Monitoring

With the *Health Monitoring* app, you can check the health of your local ABAP system.



<a name="loiobbf6b336bcb84d4185429dd76dfdfaf8__section_wqy_sp5_r5b"/>

## Context

This app allows you to monitor your system health **locally** directly on your ABAP system.

You get an overview of the metrics for the monitored system on one screen. The health metrics are represented on individual cards with a KPI that summarizes the current status and with a history of the metrics to, for example, compare trends, identify performance bottlenecks, or investigate resource shortages. 

The *Health Monitoring* app offers the following features:

-   The time filter settings apply globally to all cards on the screen, that is, to all KPIs and charts.

-   All charts are displayed on one screen and you can easily compare metrics over time.

-   Multiple characteristics are visible in one chart if applicable.


> ### Note:  
> If you want to monitor the health of multiple systems **centrally**, you can use SAP Cloud ALM. For more information, see [Central Health Monitoring Using SAP Focused Run and SAP Cloud ALM](central-health-monitoring-using-sap-focused-run-and-sap-cloud-alm-8d6e2e7.md).



<a name="loiobbf6b336bcb84d4185429dd76dfdfaf8__section_spf_zp5_r5b"/>

## Available Metrics for the ABAP Environment

In the *Health Monitoring* app, the following metrics for application checks are available for the ABAP environment:

**Metrics for the ABAP Environment in Health Monitoring**


<table>
<tr>
<th valign="top">

Metric Card



</th>
<th valign="top">

Technical Metric Name



</th>
<th valign="top">

Description



</th>
</tr>
<tr>
<td valign="top">

*ABAP Compute Units*



</td>
<td valign="top">

`abap_acu_used_count_5m`



</td>
<td valign="top">

Used quota for ABAP system memory during the last 5 minutes

A quota represents the available system size and therefore the maximum allowed consumption of a resource. A resource is measured against the quota independently. For ABAP system resources, the quota is measured in ABAP compute units \(ACUs\).

The number of ACUs on this card refers to the resource \(in this case the memory\) and its quota usage.



</td>
</tr>
<tr>
<td valign="top">

*ABAP Runtime Errors*



</td>
<td valign="top">

`abap_core_dump_count_5m`



</td>
<td valign="top">

The number of ABAP runtime errors during the last 5 minutes



</td>
</tr>
<tr>
<td valign="top">

*Application Jobs*



</td>
<td valign="top">

-   Delayed application jobs: `abap_system_appl_jobs_delayed_count_5m`

-   Failed application jobs: `abap_system_appl_jobs_failed_count_5m`

-   Running application jobs: `abap_system_appl_jobs_running_count`

-   Successful application jobs: `abap_system_appl_jobs_success_count_5m`




</td>
<td valign="top">

The number of application jobs, which includes the following:

-   The number of delayed application jobs during the last 5 minutes.

    An application job is counted as delayed when its delay exceeds a certain threshold. The default configuration uses a threshold of 60 seconds.

-   The number of failed application jobs during the last 5 minutes

-   The number of currently running application jobs

-   The number of successfully finished application jobs during the last 5 minutes


The KPI on this card refers to the number of recently failed application jobs. You can compare this value with the successfully finished application jobs to get an overview of your overall application job health.



</td>
</tr>
<tr>
<td valign="top">

*Application Logs*



</td>
<td valign="top">

`abap_system_appl_logs_count`



</td>
<td valign="top">

The total number of application logs



</td>
</tr>
<tr>
<td valign="top">

*Application Logs with Errors*



</td>
<td valign="top">

`abap_system_appl_logs_errors_count_5m`



</td>
<td valign="top">

The number of application logs with errors during the last 5 minutes



</td>
</tr>
<tr>
<td valign="top">

*Average Application Job Delay*



</td>
<td valign="top">

`abap_system_appl_jobs_avg_delay_s_5m`



</td>
<td valign="top">

Average application job delay in seconds during the last 5 minutes



</td>
</tr>
<tr>
<td valign="top">

*Captured ABAP Statistics Records*



</td>
<td valign="top">

`abap_system_ksr_captured_count_5m`



</td>
<td valign="top">

The number of ABAP statistics records that were captured by the *Capture Request Statistics* app during the last 5 minutes

In the *Capture Request Statistics* app, you can select the checkbox *Health Monitoring* for any capture profile that you create. The KPI on this card is the total number of captured ABAP statistics records during the last 5 minutes for profiles with the checkbox *Health Monitoring* selected.



</td>
</tr>
<tr>
<td valign="top">

*Current Unique Users*



</td>
<td valign="top">

-   Sessions: `abap_system_sessions_count`

-   Users: `abap_system_users_count`




</td>
<td valign="top">

The number of current unique users and sessions in the ABAP system



</td>
</tr>
<tr>
<td valign="top">

*HANA Compute Units \(CPU\)*



</td>
<td valign="top">

`hana_hcu_used_count_5m`



</td>
<td valign="top">

Used quota for SAP HANA database resources during the last 5 minutes

A quota represents the available system size and therefore the maximum allowed consumption of a resource. Each resource \(memory, disk or CPU\) is measured against the quota independently. For SAP HANA database resources, the quota is measured in HANA compute units \(HCUs\).

The number of HCUs on this card refers to the resource \(memory, disk or CPU\) with the highest quota usage.



</td>
</tr>
<tr>
<td valign="top">

*HANA Out-of-Memory Events*



</td>
<td valign="top">

`hana_db_oom_event_count_5m`



</td>
<td valign="top">

The number of out-of-memory events on the SAP HANA index server during the last 5 minutes



</td>
</tr>
<tr>
<td valign="top">

*Maximum Application Job Delay*



</td>
<td valign="top">

`abap_system_appl_jobs_max_delay_s_5m`



</td>
<td valign="top">

Maximum application job delay in seconds during the last 5 minutes



</td>
</tr>
</table>
