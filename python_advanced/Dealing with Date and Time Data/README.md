## Dealing with Date-Time Data in Python and Pandas

Date and time features are crucial in many data science applications such as forecasting, sales analysis, user behavior modeling, and resource planning. This module shows how to work with date-time data using Python’s `datetime` module and Pandas’ date-time functionality, and how to turn raw timestamps into useful features.

---

## Date-Time in Python (`datetime`, `date`, `time`, `timedelta`)

Python’s `datetime` module provides:

- `date` → calendar date (year, month, day)
- `time` → clock time (hour, minute, second, microsecond)
- `datetime` → combination of date and time
- `timedelta` → duration between two date-time values

You learn to:
- Create `date` and `time` objects and compare them to plain strings.
- Extract components such as `day`, `month`, `year`, `hour`, `minute`, `second`, `microsecond`.
- Use `datetime.now()` and `date.today()` to get the current local date and time.
- Use `.weekday()` and `.isoweekday()` to get the day of the week.
- Use `.isocalendar()` to get year, week number, and weekday.

---

## Converting Between Strings and Date-Time

Real-world datasets often store dates as strings. You use:

- `datetime.strptime()` → convert a string into a `datetime` object using format codes.
- `.date()` → extract only the date part from a `datetime`.
- `datetime.strftime()` → convert a `datetime` object into a formatted string.

Examples include converting:
- `"27 July, 2023 13:20:13"` into a `datetime` using `%d %B, %Y %H:%M:%S`.
- `"2023-07-27"` into `datetime` or `date` using `%Y-%m-%d`.
- A current `datetime` into a string like `"27/07/2023 10:59"`.

---

## Calculations with Date-Time and `timedelta`

You can compute durations by subtracting two `datetime` objects, which returns a `timedelta`. From this, you can extract:

- `duration.days`
- `duration.seconds`

You can also convert the duration into:
- hours → `duration / timedelta(hours=1)`
- minutes → `duration / timedelta(minutes=1)`
- seconds → `duration / timedelta(seconds=1)`

Additionally, you can add or subtract time from dates:
- `date + timedelta(days=2)`
- `date + timedelta(weeks=2)`

---

## Date-Time in Pandas

Pandas provides convenient tools for working with date-time data:

- `pd.to_datetime()` → converts strings into Pandas `Timestamp` objects (Pandas’ equivalent of `datetime`).
- `pd.to_timedelta()` → creates time differences similar to `timedelta`.
- `pd.date_range()` → generates sequences of dates or times given:
  - a start date
  - an end date or number of periods
  - a frequency (e.g. daily `D`, weekly `W`, minutely `T`, etc.)

Examples:
- Creating a daily date range for one month.
- Creating sequences of consecutive minutes or days starting from `datetime.today()`.

---

## Building Features from Date-Time Columns in Pandas

You create a small DataFrame with:
- `Start_date` → a sequence of timestamps (e.g. consecutive minutes)
- `End_date` → another sequence (e.g. consecutive days)
- `Target` → a random class label (1, 2, or 3)

The date columns are Pandas `Timestamp` objects. Using the `.dt` accessor, you can derive new features such as:

- `df['Day_of_end_date'] = df['End_date'].dt.day`
- `df['Month_of_end_date'] = df['End_date'].dt.month`
- `df['Year_of_end_date'] = df['End_date'].dt.year`
- `df['Weekday_of_end_date'] = df['End_date'].dt.weekday`
- `df['Hour_of_start_date'] = df['Start_date'].dt.hour`
- `df['Minute_of_start_date'] = df['Start_date'].dt.minute`

You can also compute durations between two timestamp columns:

- `df['Duration'] = df['End_date'] - df['Start_date']`
- `df['Duration_days'] = df['Duration'].dt.days`
- `df['Duration_seconds'] = df['Duration'].dt.seconds`

These derived features are very useful for feature engineering in machine learning models, where patterns often depend on time of day, day of week, or elapsed time between events.

---

## Summary

This module covers:
- Python’s `datetime`, `date`, `time`, and `timedelta` classes.
- Converting between strings and date-time objects using `strptime` and `strftime`.
- Calculating durations and manipulating dates with `timedelta`.
- Pandas tools for handling timestamps (`to_datetime`, `to_timedelta`, `date_range`).
- Creating new features from date-time columns using the `.dt` accessor.
- Computing time-based features such as day, month, week, weekday, and duration.

These techniques are essential for working with time-based data and for building robust, time-aware models in data science.

