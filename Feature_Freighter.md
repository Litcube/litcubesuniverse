# Freighter #

A simple command, the Freighter is designed to work with your dock and the dock's source stations.  Freighters should be homebased to a dock. Once the command is run, they'll use your Dockware Manager's _source_ information to figure out where to get wares required for the dock.  See the sources section of [Dockware Manager](Feature_Dockware_Manager.md).

They'll also pay attention to threshold limits on those specified sources so that your freighters aren't making multiple runs, wasting fuel, just to pick up a few wares.  See the thresholds section of [Dockware Manager](Feature_Dockware_Manager.md).

A ware set to _overstock_ will enable the Freighter to continue stocking well past its home dock's capacity limit.

Freighters do not buy wares for those wares set to _buy_.  Dock Agent does.

Freighter command requirements can be found in the [Encyclopedia](Feature_Encyclopedia_Update.md)