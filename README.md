# Persian Date(Jalali)

This is simple android calender converter for Convert Jalali date to Gregorian date.
# Gradle
```groovy
dependencies {
    compile 'com.github.samanzamani.persiandate:PersianDate:0.0.2'
}
```
## Let's convert some data :)

### Step 1

```java
PersianDate pdate = new PersianDate();
```

### step2

```java
PersianDateFormat pdformater = new PersianDateFormat();
pdformater.format(pdate);
```
***PersianDate***
---
+ **PersianDate class methods**

| method        | describtion  |
| ------------- | -----|
| PersianDate(Long timestamp)      | make time with timestamp |
| PersianDate(DATE date)      |   Constractor for make PersianDate object from Date object  |
| setShYear(int year) |    Set Jalali year |
| setShMonth(int month) |    Set Jalali month |
| setShDay(int day) |    Set Jalali day |
| setGrgYear(int day) |    Set Gregorian year |
| setGrgMonth(int day) |    Set Gregorian month |
| setGrgDay(int day) |    Set Gregorian day |
| setHour(int hour) |    Set hour of day |
| setMinute(int minute) |    Set minute of day |
| setSecond(int second) |    Set second of day |
| getShYear() |    (int) return Jalali year |
| getShMonth() |    (int) return Jalali month |
| getShDay() |    (int) return Jalali day |
| getGrgYear() |    (int) return Gregorian year |
| getGrgMonth() |    (int) return Gregorian month |
| getGrgDay() |    (int) return Gregorian day |
| getHour() |    (int) return hour of day |
| getMinute() |    (int) return minute of day |
| getSecond() |    (int) return second of day |
| getTime() |    (Long) return timestamp |
| initGrgDate() |   init date from Gregorian |
| initJalaliDate() |   init date from Jalali |
| isLeap() |   Check Jalali year is leap (TRUE-FALSE) |
| grgIsLeap() |   Check Gregorian year is leap (TRUE-FALSE) |
| toJalali(int year, int month, int day) |  Convert  Gregorian to Jalali (return int[3]) |
| toGregorian(int year, int month, int day) |  Convert  Jalali to Gregorian (return int[3]) |
| dayOfWeek() |   0-6 (0=sat) |
| getDayInYear() |   1-366 |
| dayName() |   شنبه-جمعه |
| monthName() |   فروردین-اسفند |
| getMonthDays() |   return month lenght |
| addDate() |   add some date to object |
| after(PersianDate dateInput) |   Compare 2 date (true=if input date after this) |
| before(PersianDate dateInput) |   Compare 2 date (true=if input date before this) |
| equals(PersianDate dateInput) |   Compare 2 date (true=if input date equals this) |
| untilToday() |   Cal year,month,day until now |
| getDayuntilToday() |   Cal day until now |
| toDate |   convert to Date object |


***PersianDateFormat***
---
+ **PersianDate class methods for display and parse date**
| method        | describtion  |
| ------------- | -----|
| format()      | (String) Display date |
| parse(String date,String pattern)      | (PersianDate) Convert string Jalali date (1396-05-05 & 'YYYY-MM-dd') to Persiandate |
| parseGrg(String date,String pattern)      | (PersianDate) Convert string Gregorian date (1396-05-05 & 'YYYY-MM-dd') to Persiandate |
| format()      | (String) Display date |

+ **Item for parse date**
| String key        | Role  |
| ------------- | -----|
| YYYY      | Year (1396-2012-...) |
| MM      | Month number (12-01-02-...) |
| dd      | Day number (21-01-02-...) |
| HH      | Hour  (21-01-02-...) |
| mm      | Minute  (21-01-02-...) |
| ss      | Second  (21-01-02-...) |