import datetim
import json
import os

def save_daily_log():
    today = datetime.datetime.now().strftime("%Y-%m-%d")
    log = {"last_run": today}

    with open("daily_log.json", "w") as file:
        json.dump(log, file, indent=4)

    print(f"Daily task completed on {today}")

if __name__ == "__main__":
    save_daily_log()
