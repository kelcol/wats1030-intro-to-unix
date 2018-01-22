# Stretch Goals for the *nix Scavenger Hunt

The following goals are meant to provide a way for more experienced users to
extend their knowledge of the *nix command line.

* Use `curl` to look up the URL `http://www.imdb.com/title/tt0070948/`. The title of this film will lead you to the answer. *What is the answer?*

Answer: `Zardoz`

Command:
`curl http://www.imdb.com/title/tt0070948/ | grep og:title`

Output:
```
% Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
							   Dload  Upload   Total   Spent    Left  Speed
0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0    
<meta property='og:title' content="Zardoz (1974)" />
100  127k    0  127k    0     0   125k      0 --:--:--  0:00:01 --:--:--  135k
```
