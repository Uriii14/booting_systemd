In order to execute the program, these are the steps to follow.

1. Copy the script and make sure it is executable:
   `sudo cp hello.sh /usr/local/bin/hello.sh`
   `sudo chmod +x /usr/local/bin/hello.sh`
2. Copy the unit file:
   `sudo cp hello.service /etc/systemd/system/`
3. Reload systemd, enable the service and start it:
   `sudo systemctl daemon-reload`
   `sudo systemctl enable --now hello.service`
4. Check the output:
    `journalctl -u hello.service -b --no-pager`
    Where -b and --no-pager are optional.
    -b shows only the current boot, removing everything else in the journal.
    --no-pager prints it directly in the terminal, getting your prompt back instead of having to leave from the execution.
