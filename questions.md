# Congestion Tax Calculator

### Visit [README.md](README.md) for architecture design and other documents.

## Enhancements

### 1 - Multi-tenancy
    The entire application is built as per the multi-tenancy architecture. With the same instance, we will be able to configure N number of cities.

### 2 - Data are configurable
    Almost all the properties or conditions are moved to the database. So any changes in the city can be modified effortlessly.

### 3 - No tax for days before the public and after a holiday
    Additionally added after holiday also no tax day which is again configurable.

### 4 - Change in tariff pattern (modification in data presentation)
    The tariff for 18:30–05:59 is configued as 18:30 to 11:59 and 00:00 to 05:59 for better calculation.

### 5 - Extended support for all years (2013)
    The tax calculator will not serve only for 2013, but it also serves any data belonging to any year.

##  Questions and suggestions

### The single charge rule

- Check-In and Check-Out: Suppose if 18:30–05:59 was not free, then the vehicle is crossing at yesterday 23:55 and the next toll within one hour.
  - [x] since the last two transactions happened within one hour, the maximum will be the tax amount for the respective day.
  - [ ] do we need to consider as two different payments?


## Clarification
    Given: The maximum amount per day and vehicle is 60 SEK.
    Implemented: Assuming that the maximum amount per single day for a specific vehicle is 60 SEK.
