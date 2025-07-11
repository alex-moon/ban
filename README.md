# Self-imposed ban

A lightweight Bash script to help you block yourself from using time-wasting or
distracting commands until a specified date with optional reasons and friendly reminders.

Perfect for developers and terminal junkies trying to reclaim their focus.

## Install

Simply download the ban script into your `~/bin` directory or any directory in your `$PATH`
and make it executable.

```bash
mkdir -p ~/bin
curl -o ~/bin/ban https://raw.githubusercontent.com/alex-moon/ban/refs/heads/main/ban
chmod +x ~/bin/ban
```

## Usage

When you ban a command, attempting to run it will result in a friendly reminder
that you have banned it, along with any reasons you provide, and a date the ban
will be lifted. Reasons and expiration dates are both optional - if the date
is not provided, the ban will expire 40 days from now.

```bash
# these are all valid commands:
ban steam
ban steam 'I have been spending too much time playing games'
ban steam 'I have been spending too much time playing games' 2025-08-20
```

To unban a command, simply remove the command from your `~/.bans` directory:
```bash
rm ~/.bans/steam
```

To see a list of all your current bans, simply index the `~/.bans` directory:
```bash
ls ~/.bans
```

## Uninstall
To uninstall the ban script, simply remove the `ban` file from your `~/bin` directory
and delete the `~/.bans` directory.

```bash
rm ~/bin/ban
rm -rf ~/.bans
```

## Contributing

Contributions are welcome! If you have suggestions for improvements or new features,
please open an issue or submit a pull request.
