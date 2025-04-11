# International transport support data
*Applications from 2023 and 2024 for the Danish international transport support fund owned by Statens Kunstfond and administered by the genre organisations Art Music Denmark, JazzDanmark, ROSA, and Tempi. Data is organized like a relational database with four tables (applications, activities, participants and reports - the description of which can be read below). 
They all share the same primary key called j_nr. The relationship between applications and the other tables is a one-to-many relationship - in practice though, the relationship to reports is a one-to-one relationship.*


*For any questions please contact morten@genreorganisationerne.dk.*


##  nat_transport_applications.csv 

| Field | Type | Description |
|--------------|------|-------------|
| id | character | NA |
| application_date_estimated | Date | NA |
| application_period | character | NA |
| genre | character | NA |
| application_postcode | character | NA |
| shows_count | numeric | NA |
| act_name | character | NA |
| was_approved | logical | NA |
| granted | numeric | NA |
| women_count | character | NA |
| men_count | character | NA |
| nonbinaries_count | character | NA |
| show_date | Date | NA |
| show_postcode | character | NA |
| show_city | character | NA |
| show_venue | character | NA |
| show_audience_estimated | numeric | NA |
| show_members_count | character | NA |
| show_application_amount | numeric | NA |
| show_bridge_ferry | character | NA |

**int_transport_activities.csv**

*Activities related to applications. We call them activities and not concerts because they're not all concerts but can also be other kinds of international travel related to music.*

| Field | Type | Description |
|--------------|------|-------------|
| j_nr | character | Application id |
| activity_id | character | Activity id |
| activity_type | character | Activity type - i.e. concert or other |
| activity_country | character | Country where activity took place |
| activity_city | character | City where activity took place |
| activity_city_latitude | numeric | latitude of activity city |
| activity_city_longitude | numeric | longitude of activity city |
| activity_venue | character | Venue where activity took place |
| activity_venue_web | character | Website of activity venue |
| activity_fee | numeric | Fee received for activity |
| activity_fee_currency | character | Currency of activity fee |

**int_transport_participants.csv** 

*Participants related to applications - i.e. members of a the travelling party. For each application we get the number of males, females and non-binaries within each age group.*

| Field | Type | Description |
|--------------|------|-------------|
| j_nr | character | Application id |
| participant_group_id | character | Participant group id |
| participant_gender_group | character | Gender group, i.e. males, females or non-binaries |
| participant_age_under18 | numeric | Number of people under 18 within the gender group |
| participant_age_18_24 | numeric | Number of people in age span 18-24 within the gender group |
| participant_age_25_29 | numeric | Number of people in age span 25-29 within the gender group  |
| participant_age_30_39 | numeric | Number of people in age span 30-39 within the gender group  |
| participant_age_40_49 | numeric | Number of people in age span 40-49 within the gender group  |
| participant_age_50_59 | numeric | Number of people in age span 50-59 within the gender group  |
| participant_age_60_over | numeric | Number of people age 60 or more within the gender group  |

**int_transport_reports.csv** 

*Data from final reports, which are submitted upon completion of the tour/international travel project. Contains final accounts and evaluation of the project. Each evaluating question has the possibility to submit comments but these have been removed from the public data set as they may contain personal information.*

| Field | Type | Description |
|--------------|------|-------------|
| j_nr | character | Application id |
| report_id | character | Report id |
| accounts_expenses_fee_total | numeric | Final accounts expense item: fees paid to musicians |
| accounts_expenses_accommodation | numeric | Final accounts expense item: accommodation expenses |
| accounts_expenses_meals | numeric | Final accounts expense item: meals |
| accounts_expenses_pr | numeric | Final accounts expense item: PR |
| accounts_expenses_backline | numeric | Final accounts expense item: backline rental |
| accounts_expenses_local_transport | numeric | Final accounts expense item: local transport expenses |
| accounts_expenses_international_transport | numeric | Final accounts expense item:  international transport expenses |
| accounts_expenses_other | numeric | Final accounts expense item: other |
| accounts_expenses_total | numeric | Expenses total |
| accounts_income_fee_total | numeric | Final accounts income item:  show fees |
| accounts_income_grants | numeric |  Final accounts income item: grants |
| accounts_income_funds | numeric | Final accounts income item: other funds (not including this fund) |
| accounts_income_merchandise | numeric | Final accounts income item: merchandise |
| accounts_income_own_contribution | numeric | Final accounts income item: own contribution |
| accounts_income_other | numeric | Final accounts income item: other |
| accounts_income_estimated_total | numeric | Income total |
| accounts_result | numeric | result |
| accounts_comments | character | Comments for accounts |
| evaluation_further_opportunities | character | Likert scale rating of the question: I hvor høj grad oplever du, at dit/jeres projekt har skabt yderligere muligheder for internationale aktiviteter? |
| evaluation_artistic_development | character | Likert scale rating of the question: I hvor høj grad oplever du, at projektet har bidraget til din/jeres kunstneriske udvikling? |
| evaluation_satisfaction | character | Likert scale rating of the question: Hvor tilfreds er du med ansøgningsprocessen? |
