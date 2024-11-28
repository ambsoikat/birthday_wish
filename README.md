from datetime import datetime, timedelta
import time

# Friend's name and birthday
friend_name = "Ishee"
birthday_date = datetime(2024, 11, 28)  # Today's date

# Function to display the countdown
def countdown_to_birthday():
    while True:
        now = datetime.now()
        time_left = birthday_date - now

        if time_left <= timedelta(0):
            print(f"\n🎉 Happy Birthday, {friend_name}! 🎂🎈 Wishing you a day filled with joy and laughter! 🎁🎊")
            break

        days = time_left.days
        hours, remainder = divmod(time_left.seconds, 3600)
        minutes, seconds = divmod(remainder, 60)

        print(f"\rCountdown to {friend_name}'s birthday: {days}d {hours}h {minutes}m {seconds}s", end="")
        time.sleep(1)

# Start the countdown
countdown_to_birthday()
