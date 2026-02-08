# Nested-logic-issue-in-hackkerank
Python program that calculates a library book fine based on actual and expected return dates. It compares year, month, and day to apply the correct penalty using standard rules (no fine, daily, monthly, or fixed yearly fine). Clean logic, beginner-friendly, and suitable for coding challenge practice and date-based condition handling examples.
# Enter your code here. Read input from STDIN. Print output to STDOUT
r_day, r_month, r_year = map(int, input().split())
d_day, d_month, d_year = map(int, input().split())
fine = 0
if r_year > d_year:
    fine = 10000
elif r_year == d_year:
    if r_month > d_month:
        fine = 500 * (r_month - d_month)
    elif r_month == d_month and r_day > d_day:
        fine = 15 * (r_day - d_day)
print(fine)
