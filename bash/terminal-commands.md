# tar files
tar xvf [filename]

# Log the output of a command

## write it to a log but hide it from live execution
[command] > [file.log] 2>&1

## see the output live while also saving it
[command] 2>&1 | tee [file.log]


