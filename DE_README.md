# DE-TAKE-HOME
**Take home challenge for Data Engineer position at Easyship, Thank you showing your interest**

**This assignment consists of 2 parts : 1. Develop data mart from source tables 2. Automate the pipeline to run daily at 9AM UTC**

**Feel free to use any programming language and tool to acheive the goal : The idea is to generate data mart and refresh everyday to be used by the visualisation layer**

**Remember the visualisation layer only uses the snapshot**

**Good luck**
---

Following are the tables that will be required for assignment completion : 

Table containing the list of all the clients at Easyship 

| es\_clients          |
| -------------------- |
| easyship\_client\_id |
| name                 |
| onboarding\_date     |
| country\_id          |
| classification\_id   |
| is\_active           |

Table containing list of all the couriers that are integrated with Easyship

| es\_couriers            |
| ----------------------- |
| easyship\_courier\_id   |
| name                    |
| umbrella\_name |
| supported\_services     |
| does\_pickup            |
| tracking_rating         |
| is\_active              |

Table containing shipment details

| es\_shipments             |
| ------------------------- |
| easyship\_shipment\_id    |
| easyship\_client\_id      |
| easyship\_courier\_id     |
| origin\_country\_id       |
| destination\_country\_id  |
| last\_status\_message\_id |
| label\_paid\_at           |
| total\_volumetric\_weight |

Shipment items table contains all the items within individual shipment

| es\_shipment\_items          |
| ---------------------------- |
| easyship\_shipment\_item\_id |
| easyship\_shipment\_id       |
| item\_category\_id           |
| volumetric\_weight           |
| contains\_battery            |

Status Records Table contain all the shipment tracking events 

| status\_records        |
| ---------------------- |
| status\_record\_id     |
| status\_message\_id    |
| easyship\_shipment\_id |
| created\_at            |

Status Messages is mapping table

| status\_messages    |
| ------------------- |
| status\_message\_id |
| name                |

Countries is a mapping table

| countries   |
| ----------- |
| country\_id |
| name        |
| region      |

---

Data can be accessed on BigQuery, HR must have provided you with dataset link. Please reach out to HR if you don't have the link yet.

---

**Scenario :**

1. Operations Team would like to know what are the top 3 performing couriers in the month of June, July and August 2021. Performance is calculated based on the number of shipments. 

2. Business Team would like to know which couriers are used most on each day of the week. So the output will look like

| day\_of\_week | courier\_name                  |
| ------------- | ------------------------------ |
| Monday        | uxpx - priority mail           |
| Tuesday       | qxprexx - domextic             |
| Wednesday     | uxpx - firxt claxx             |


Feel free to reach out to HR in case of any queries.