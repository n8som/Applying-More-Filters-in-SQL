# Applying-More-Filters-in-SQL

<h2>Activity overview</h2>

As a security analyst, I’ll often need to query numbers and dates.

For example, I may need to filter patch dates to find machines that need an update. Or I might filter login attempts made during a certain period to investigate a security incident.

Common operators for working with numeric or date and time data will help I accurately filter data. These are some of the operators I'll use:

- = (equal)
- ">" (greater than)
- < (less than)
- <> (not equal to)
- ">=" (greater than or equal to)
- <= (less than or equal to)

In this lab activity, I’ll apply these operators to accurately filter for specific numbers and dates!

Note: The terms row and record are used interchangeably in this lab activity.

<h2>Scenario</h2>

  In this scenario, I’m investigating a recent security incident.

I need to gather information about login attempts for certain dates and times. This will help in resolving a security incident.

Here’s how I’ll do this task: First, I’ll retrieve login events made after a certain date. Second, I’ll narrow the focus of the search to filter logins in a date range. Third, I’ll investigate logins that were made at certain times. Finally, I’ll filter login attempts based on their event IDs.

<h2>Task 1. Retrieve login attempts after a certain date</h2>

In this task, I need to investigate a recent security incident. To do this, I need to gather information about login attempts made after a certain date.

1. Complete the SQL query to retrieve data for login attempts made after '2022-05-09'. Replace X with the correct operator:

```SELECT *```

```FROM log_in_attempts```

```WHERE login_date > '2022-05-09';```

Here I see there were 25 login attempts made after 2022-05-09:

![image](https://github.com/n8som/Applying-More-Filters-in-SQL/assets/110139109/082f2cfd-c340-4df7-a919-5e44676751fc)

Now, based on my first query, I find a need to expand the date range to include 2022-05-09 in my search.

2. Complete the SQL query to retrieve data for login attempts that were made on or after '2022-05-09'. Replace X with the correct operator:

```SELECT *```

```FROM log_in_attempts```

```WHERE login_date >= '2022-05-09';```

Here I see there were 165 login attempts made on or after 2022-05-09:

![image](https://github.com/n8som/Applying-More-Filters-in-SQL/assets/110139109/b0c74a8b-76ee-4d86-bd5d-98afa7f0d26a)

<h2>Task 2. Retrieve logins in a date range</h2>

In this task, I need to narrow the focus of the search. Login attempts made after 2022-05-11 shouldn't be included. Use the ```BETWEEN``` and ```AND``` operators to return results between '2022-05-09' and '2022-05-11'.

- Run the query to retrieve the required records. I must insert the required dates X and Y:

```SELECT *```

```FROM log_in_attempts```

```WHERE login_date BETWEEN '2022-05-09' AND '2022-05-11';```

There were 123 login attempts made between 2022-05-09 and 2022-05-11:

![image](https://github.com/n8som/Applying-More-Filters-in-SQL/assets/110139109/b57e9f3f-cddb-4217-8485-6606c32e6a68)

<h2>Task 3. Investigate logins at certain times</h2>

In this task, I need to investigate logins that were made at certain times. To do this, filter the data in the ```log_in_attempts``` table by login time (login_time).

First, my organization's typical work hours begin at 07:00:00. Retrieve all login attempts made before 07:00:00 to learn more about the users who are logging in outside of typical hours.

1. Write a SQL query to retrieve data for login attempts made before '07:00:00'.

Note: Place time data in single quotation marks.

Here I see the username, eraab, was the fifth record returned from this query:

![image](https://github.com/n8som/Applying-More-Filters-in-SQL/assets/110139109/7fd9dc81-61ad-4853-add8-2df2b64084aa)

The query in the previous step returned more results than required.

2. Modify the query to return logins between '06:00:00' and '07:00:00'.

Here I see the earliest login attempt between 06:00:00 and 07:00:00 was lyamamot at '06:01:31' :

![image](https://github.com/n8som/Applying-More-Filters-in-SQL/assets/110139109/00e683b7-39c1-4774-8dd6-586cb2ae3c95)

<h2>Task 4. Investigate logins by event ID</h2>

In this task, I need to investigate login attempts based on event ID numbers. With this query, I want to return only the ```event_id```, ```username```, and ```login_date``` fields from the ```log_in_attempts``` table.

Note: The event_id column contains numeric data; do not place numeric data in quotation marks.

1. Write a query to return login attempts with ```event_id``` greater than or equal to 100.

Here I see the login date of the third result returned 2022-05-09 :

![image](https://github.com/n8som/Applying-More-Filters-in-SQL/assets/110139109/956f521b-1366-4e1e-9a87-04f121a74a8b)

The query in the previous step returned more data than required.

2. Modify the query to return only login attempts with ```event_id``` between 100 and 150.

Here is the username, tmitchel, is the seventh result returned:

![image](https://github.com/n8som/Applying-More-Filters-in-SQL/assets/110139109/2a527798-9a8f-4633-b48a-11c113c0bdb8)

<h2>Conclusion</h2>

I have completed this activity and practiced applying

- the ```WHERE``` keyword
- the ```BETWEEN``` and ```AND``` operators, and
- operators for working with numeric or date and time data types (for example, =, >, >=)

to filter data from a table.

I’m now ready to filter for numbers and dates to extract all sorts of useful data!

