# Loki Render

Loki Render allows you to create your own Blender render farm, serving Blender render jobs to a group of computers. Loki is easy to setup and runs on Linux, Windows, or Mac, making it a quick and flexible distributed network rendering solution!

This is a fork of Mike Peralta's LokiRender adaptation for Blender 2.80 (and higher) of the original project by Daniel Petersen over on [Sourceforge](https://sourceforge.net/projects/loki-render/). 

##	Workflow

A typical workflow to start utilizing Loki Render, is something like:

1. Pick a machine to be the master, and start Loki Render in "Master" mode (or in "Master+Grunt" mode)
2. Start Loki Render in Grunt mode on some other machines
3. Configure the Master
4. Configure the Grunts
	* If you're on a simple home LAN, the Grunts should automatically detect the Master
	* Otherwise, you'll want to configure the Master IP address in their settings
5. Add some jobs to the Master
6. Start rendering, on the Master

## Prerequisites

You should have either Oracle's JDK 8 or OpenJDK 8 installed. This project is mostly tested on Linux, but should also work on Windows and Mac as well.

## Getting Started

* First make sure you have java installed on your computer. You can install OpenJDK 11 on Ubuntu with 
```
sudo apt-get install openjdk-11-jdk
```
* Then, of course, you will want to grab the latest LokiRender for Blender 2.80 JAR file from the [release page](https://github.com/straaljager/loki-render/releases), and save it somewhere
* You can then launch Loki Render with a simple command:

```
java -jar LokiRender-<version>.jar [<path-to-BlenderExe>] [MasterIP]
```

For example:
```
java -jar LokiRender-2.80.jar /usr/bin/blender 123.456.789.001
```

* Replace <version> to match the jar file you have
* Add the full path to the Loki Render jar file if you wish to run the command outside the directory where the jar is stored
* Use [\<BlenderExe\>] by adding the path to a Blender executable, to start Loki Render in grunt mode without the GUI (great for headless rendering)
* Use [\<MasterIP\>] to specify the IP address of a server running Loki Render in Master mode, otherwise Loki Render will attempt to auto detect

Other examples:
```
java -jar LokiRender-2.80.jar
java -jar LokiRender-2.80.jar /path/to/blender
java -jar LokiRender-2.80.jar 192.168.17.45
java -jar LokiRender-2.80.jar /path/to/blender 192.168.17.45
java -jar /path/to/jar/folder/LokiRender-2.80.jar /path/to/blender 192.168.17.45
```

## Further Information

More in depth information will eventually be made available in the [Wiki](https://github.com/mikeperalta1/loki-render/wiki) section.

## Built With

* Netbeans IDE 8.1

## Contributing

* Please feel free to send bug fixes and improvements for consideration. I may not be able to put much time into this project, so it needs support from the community.
* If you can't contribute code, but would still like to help, please consider contributing to the [Wiki](https://github.com/mikeperalta1/loki-render/wiki).
I would like the goal of the Wiki to become an easy guide even for those who are not technically inclined.

###	Code Styling

TO-DO

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/mikeperalta1/loki-render/tags). 

## Authors

* **Daniel Petersen** - *Initial work* - [Original Project](https://sourceforge.net/projects/loki-render/)
* **Mike Peralta** - *Reviving bug fix and fork to this repo* - [Music](http://MikePeralta.com/)

See also the list of [contributors](https://github.com/mikeperalta1/loki-render/contributors) who participated in this project.

## License

This project is licensed under the [GPL v3 License](https://www.gnu.org/licenses/gpl-3.0.en.html) - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Huge thanks to Daniel Petersen for creating this wonderful and fun project in the first place, creating his initial wiki with useful starter information, and giving his blessing for this fix+fork to happen
* The wonderful people working on Blender
* [PurpleBooth](https://gist.github.com/PurpleBooth/) for this README [template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2)
* My dog



