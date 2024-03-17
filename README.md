# Chart Activity Flatpak

 Chart lets you do graphical representation of simple tabular data, in the form “label: value”. It can draw Horizontal/Vertical bar charts, line charts and pie charts.

 To know more refer https://github.com/sugarlabs/chart

 ## How To Build

 ```
 git clone https://github.com/flathub/org.sugarlabs.Chart.git
 cd org.sugarlabs.Chart
flatpak --user remote-add --if-not-exists flathub-beta https://flathub.org/beta-repo/flathub-beta.flatpakrepo
flatpak -y --user install flathub-beta org.gnome.{Platform,Sdk}//46beta
flatpak -y --user install org.sugarlabs.BaseApp//24.04
 flatpak-builder --user --force-clean --install build org.sugarlabs.Chart.json
 ```

 ## Check For Updates

 Install the flatpak external data checker
 ```
 flatpak --user install org.flathub.flatpak-external-data-checker
 ```

 Now to update every single module to the latest stable version use
 ```
 cd org.sugarlabs.Chart
 flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.Chart.json
 ```