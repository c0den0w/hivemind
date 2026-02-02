[[#Pipewire]] is a software that handles #audio and #video in [[#linux]] environments, this usually run as user service so use the --user argument

`systemctl --user restart pipewire.service pipewire-pulse.service wireplumber.service`

this command starts the #PipeWire service and enables the use of USB headsets (Not Type C)
