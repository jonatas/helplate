# Helplate 

This is a nice command line to help you to use your own template. Using liquid template, this command line receives the template name as the first param. All other params is a key=value params, that will be used on the template.


This is a example, like project file in this repo containing:

  Project: {{ name }}'s project

  [ Participants ]

  Theres some participants: {{ participants | join glue: ', '}}

  help:
  participants: who are envolved in this project? customers, clients etc (divided by comma)

And executing template with params:

 jonatas@xonatax-mac: helplate $ ./helplate project name=comodities
 who are envolved in this project? customers, clients etc (divided by comma)
 jonatas, angela, pedro, paul   


And this will puts:

 Project: comodities's project

 [ Participants ]

 Theres some participants: jonatas, angela, pedro, paul

