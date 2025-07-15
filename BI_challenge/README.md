# bi-take-home

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

Download CSV files

---

**Scenario :**

1. Operations Team would like to know what are the top 3 performing couriers in the month of June, July and August 2021. Performance is calculated based on the number of shipments. 


2. The pricing Team will be adjusting margin based on shipment volume.  Could you help them identify what was the % growth in terms of shipment for 2 consecutive weeks? They would only like to see the result for these couriers umbrella names (fedex and uxpx) and for the week that starts on 6-Sept-2021 compared to the week that starts on 30-Aug-2021.

PS : Week starts on Monday and ends on Sunday

3. Customer Success Team would like to know the average delivery times broken down by month and courier name in the month of June, July and August 2021. Delivery time starts when a shipment has first status record event within (`In Transit to Customer, In Transit to Consolidation Center`) and Ends when there is first status record event within (`Delivered, Out for Delivery, Failed Delivery Attempt, Delivery Expected (End of Updates)`)


4. Business Team would like to know which couriers are used most on each day of the week. So the output will look like

| day\_of\_week | courier\_name                  |
| ------------- | ------------------------------ |
| Monday        | uxpx - priority mail           |
| Tuesday       | qxprexx - domextic             |
| Wednesday     | uxpx - firxt claxx             |


5. Marketing Team would like to know, on average how much time does it take for a client to get activated. Activation Time is calculated from onboarding to the first shipment made


Good Luck and Feel free to reach out to HR in case of any queries.
