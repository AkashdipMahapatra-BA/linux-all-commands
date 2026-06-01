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

> Action: Extracts and prints every line that contains the exact case-sensitive string "ERROR".
>   * Use case: Best for a quick glance at explicit error messages.
 
---

* grep -c "ERROR" /path/to/logfile.log

> Action: Counts the total number of lines matching "ERROR" instead of displaying the actual text.
>  * Use case: Ideal for generating statistics or checking if errors occurred during a specific time frame.
 
---

* grep -i "error" /path/to/logfile.log

> Action: Performs a case-insensitive search, capturing variations like "error", "ERROR", "Error", or "ErRoR".
>  * Use case: Crucial when you aren't sure how the logging framework formats its text.
 
---

* grep -n "ERROR" /path/to/logfile.log

> Action: Displays the matching lines along with their exact line numbers from the file.
> * Use case: Perfect for navigating directly to the problem area inside a heavy log file using text editors like vim or nano.
 
---

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/b34f0bb0-ab72-401a-8c16-bc382703e422" />


## Quick Reference Comparison

| Command [7, 8, 9] | Case Sensitive? | Output Type | Best For |
|---|---|---|---|
| grep | Yes | Matching text lines | Direct log scanning |
| grep -c | Yes | An integer (count) | Metric reporting |
| grep -i | No | Matching text lines | Flexible string catching |
| grep -n | Yes | Line number + text | Quick file editing |
