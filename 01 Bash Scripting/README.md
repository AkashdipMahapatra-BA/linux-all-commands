## `bash scripting` practice with `WSL/Ubuntu`

---

# Move the logs file to Linux

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/a8b0892c-5325-4ae3-ba27-4db5a940f6ef" />
</br>

```
mkdir -p ~/bash_practice/logs
```

### Component Breakdown

* `mkdir`: The "make directory" command used to create new folders.
* `-p`: The "parents" flag. This creates any missing parent folders in the path automatically. It also prevents an error if the folder already exists.
* `~/`: A shortcut that represents your user's personal home directory (e.g., /home/username/).
* `bash-practice/logs`: The specific folder structure you want to build.

---

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/c50242e0-c0bf-45d6-8aa3-3aeafb70a121" />

---

* grep "ERROR" /path/to/logfile.log

> Action: Extracts and prints every line that contains the exact case-sensitive string "ERROR". </br>
> Use case: Best for a quick glance at explicit error messages.
 
---

* grep -c "ERROR" /path/to/logfile.log

> Action: Counts the total number of lines matching "ERROR" instead of displaying the actual text. </br>
> Use case: Ideal for generating statistics or checking if errors occurred during a specific time frame.

<img width="862" height="112" alt="image" src="https://github.com/user-attachments/assets/d09ca56b-96fb-4348-9bc2-701c79e29ff0" />

---

* grep -i "error" /path/to/logfile.log

> Action: Performs a case-insensitive search, capturing variations like "error", "ERROR", "Error", or "ErRoR". </br>
> Use case: Crucial when you aren't sure how the logging framework formats its text.

<img width="1366" height="180" alt="image" src="https://github.com/user-attachments/assets/f70f9440-6b1f-43bb-aadc-f367f9c9a10e" />

---

* grep -n "ERROR" /path/to/logfile.log

> Action: Displays the matching lines along with their exact line numbers from the file. </br>
> Use case: Perfect for navigating directly to the problem area inside a heavy log file using text editors like vim or nano.

<img width="1366" height="150" alt="image" src="https://github.com/user-attachments/assets/f22c9442-afd4-4def-a258-4e6765454e6b" />
 
---

## Quick Reference Comparison

| Command [7, 8, 9] | Case Sensitive? | Output Type | Best For |
|---|---|---|---|
| grep | Yes | Matching text lines | Direct log scanning |
| grep -c | Yes | An integer (count) | Metric reporting |
| grep -i | No | Matching text lines | Flexible string catching |
| grep -n | Yes | Line number + text | Quick file editing |
