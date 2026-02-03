import os
import shutil

source = "/home/user/.local/share/Steam/steamapps/common/SimCity 3000 Unlimited/Cities"
destin = "/path/to/backup/"

ignore = [
    "Berlin, Germany.sc3",
    "Craterville.sc3",
    "Europolis.sc3",
    "Farmsville.sc3",
    "Frankfurt, Germany.sc3",
    "Liverpool, England.sc3",
    "London, England.sc3",
    "Madison, WI.sc3",
    "Madrid, Spain.sc3",
    "Moscow, Russia.sc3",
    "Mount Herrang.sc3",
    "Roadless Paradise.sc3",
    "Sacramento, CA.sc3",
    "Seoul, Korea.sc3",
    "steam_autocloud.vdf",
    "TUTORIAL.SC3",
]

os.makedirs(destin, exist_ok=True)

def backup():
    for name in os.listdir(source):
        print(f"Found {name}")
        if name in ignore:
            print("Ignoring")
            continue
        src = os.path.join(source, name)
        if os.path.isdir(src):
            print("Ignoring")
        dst = os.path.join(destin, name)
        if os.path.isfile(src):
            shutil.copy2(src, dst)
            print("Copied")

def restore():
    for name in os.listdir(destin):
        print(f"Found {name}")
        src = os.path.join(destin, name)
        dst = os.path.join(source, name)
        if os.path.isfile(src):
            shutil.copy2(src, dst)
            print("Copied")

while True:
    print("\nMenu\n")
    print("'backup' to backup cities")
    print("'restore' to restore cities from backups")
    print("'exit' to exit\n")
    choice = input(">").strip()

    if choice == "backup":
        backup()
    elif choice == "restore":
        restore()
    elif choice == "exit":
        break
    else:
        print("Invalid")
