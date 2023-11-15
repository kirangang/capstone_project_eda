# Hotel Booking Analysis Project

Welcome to the Hotel Booking Analysis project repository. This project focuses on exploring and analyzing data related to hotel bookings to gain insights and make data-driven decisions in the hospitality industry. This README provides an overview of the project, its goals, and how to use the code and data provided in this repository.

## Introduction

The hotel industry relies heavily on data-driven decision-making to optimize pricing, occupancy, and customer satisfaction. This project aims to conduct an Exploratory Data Analysis (EDA) on a dataset containing information about hotel bookings to uncover trends, patterns, and insights that can help hotels and stakeholders in the industry make more informed decisions.

## Dataset

We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel, and includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things.

 It contains the following columns.

- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status.

Total number of rows in data: 119390
Total number of columns: 32

## Data Cleaning and Feature Engineering
**1) Removing Duplicate rows**
     - All duplicate rows were dropped.
**2) Handling null values**
    - Null values in columns company and agent were replaced by 0.
    - Null values in column country were replaced by 'others'.
    - Null values in column children were replaced by the mean of the column.
**3) Converting columns to appropriate data types**
    - Changed data type of children, company, agent to int type.
    - Changed data type of reservation_status_date to date type.
**4) Removing outliers**
    - One outlier was found in the adr column. Simply dropped it.
**5) Creating new columns**
    - Created new column total_stay by adding stays_in_weekend_nights+stays_in_week_nights.
    - Created new column total_people by adding adults+children+babies

## Exploratory Data Analysis
**Performed EDA and tried answering the following questions:**

1) Which type of hotel is mostly prefered by the guests?
2) Which distribution channel is mostly used for hotel bookings?
3) Which agent made the maximum bookings?
4) What is the percentage of repeated guests?
5) Which type of food is mostly preferred by the guests?
6) Which is the most preferred room type by the customers?
7) What is the pecentage of cancellation?
8) From which country the most guests are coming?
9) In which month most of the bookings happened?
10) Which year had the highest bookings?
11) Which Hotel type has the highest ADR?
12) Which hotel has longer waiting time?
13) Which market segment has the higest cancellation rate?
14) What is the ADR across different months?
15) Which distribution channel contributed more to adr in order to increase the the income?

Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:

Bar Plot.

Scatter Plot.

Pie Chart.

Line Plot.

Heatmap.

Pair Plot

## Univariate Analysis:
Performed univariate analysis and made following conclusions:
1) City Hotel is most preffered hotel by guests.
2) Most 79% people prefer'TA/TO' for booking.
3) Agent ID number 9 made most of the bookings.
4) Only 4% people are repeated guests.
5) The most preferred meal type by the guests is BB (Bed and Breakfast).

## Bivariate Analysis 
 We tried to answer following questions

 1) Overall adr of City hotel is slightly higher than Resort hotel and no. of bookings of City hotel is also higher than Resort hotel. Hence, City hotel makes 
   more revenue.
 2) City hotel has slightly higher median lead time. Also median lead time is significantly higher for both hotels, this means customers generally plan their 
    hotel visits way early.
 3) Almost 30% of city Hotel bookings got canceled.
 4) Both hotels have very small percentage that customer will repeat, but resort hotel has slightly higher repeat percentage than city Hotel.
 5) TA/TO is mostly used for planning hotel visits well ahead of time. 
 6) While booking via TA/TO one may have to wait a little longer to confirm booking of rooms.
 7) GDS channel brings higher revenue generating deals for city hotel, in contrast to that most bookings come via TA/TO. City Hotel can work to increase outreach 
    on GDS channels to get more higher revenue generating deals.
 
## Conclusion
 1) City hotel is the most preferred hotel type by the guests. We can say City hotel is the busiest hotel.

 2) Most of the bookings were made through TA/TO (Travel agents/Tour operators).

 3) Only 4% people have revisited the hotels. Rest 96% were new guests. Thus retention rate is low.

 4) BB(Bed & Breakfast) is the most preferred type of meal by the guests.

 5) Maximum number of guests were from Portugal, i.e. more than 25000 guests.

 6) 27.5% bookings were got cancelled out of all the bookings.

 7) Most of the bookings for City hotels and Resort hotels were happened in 2016.

 8) Average ADR for city hotel is high as compared to resort hotels. So city hotels are generating more revenue than the resort hotels.

 9) Agent number 9 made most of the bookings.

 10) Waiting time period for City hotel is high as compared to resort hotels. That means city hotels are much busier than Resort hotels.

 11) Room type A is the mostly preferred room type.

 12) Optimal stay in both type of hotel is less than 7 days. Usually people stay for a week.

 13) If number of people is more then ADR also increases means revenue increases.

 14) Most of the bookings were done in the month of July and August.

## Challenges
 1) There was a lot of duplicate data.

 2) Data was present in wrong datatype format.

 3) Choosing appropriate visualization techniques to use was difficult.

 4) A lot of null values were there in the dataset.

