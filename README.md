# threadfin-unraid
threadfin xml template for unraid

Having a hard time with Xteve so i tried Threadfin. Much better and reliable!<br><br>

I added Samsung Tv Plus M3u and Xml guide feed to Threadfin, <br>
Playlist URL link, https://i.mjh.nz/SamsungTVPlus/us.m3u8 <br>
XMLTV URL link, https://i.mjh.nz/SamsungTVPlus/us.xml <br>
Threadfin setttings: <br>
EPG Source: XEPG<br>
Stream Buffer: FFmpeg<br>
Click Server Information on top right corner find your Stream Information<br>
copy the M3U URL to Jellyfin >dashboard >livetv >Tuner Devices> in M3U Tuner and click save<br>
copy the XMLTV URL to Jellyfin >dashboard >livetv > TV Guide Data Providers > in XMLTV and click save<br>
Click Refresh Guide Data in Jellyfin<br>

Mapping categories in Threadfin:<br>
goto Threadfin web and click Mapping<br>
click individual channel and select EPG Category: (Kids, News, Movie, Series, Sports)  and click Save<br><br>

Its better to restart both Threadfin and Jellyfin after Mapping<br>
<br><br>
<img src="https://github.com/jjone/threadfin-unraid/blob/main/Snipaste_2024-05-19_11-22-40.png">
<br><br>
unraid file location

/boot/config/plugins/dockerMan/templates-user/my-Threadfin.xml

`
`````
<?xml version="1.0"?>
<Container version="2">
  <Name>Threadfin</Name>
  <Repository>fyb3roptik/threadfin</Repository>
  <Registry/>
  <Network>bridge</Network>
  <MyIP/>
  <Shell>sh</Shell>
  <Privileged>false</Privileged>
  <Support/>
  <Project/>
  <Overview/>
  <Category/>
  <WebUI>http://[IP]:[PORT:34400]/web/</WebUI>
  <TemplateURL/>
  <Icon>https://raw.githubusercontent.com/Threadfin/Threadfin/main/html/img/threadfin.ico</Icon>
  <ExtraParams/>
  <PostArgs/>
  <CPUset/>
  <DateInstalled>1715733849</DateInstalled>
  <DonateText/>
  <DonateLink/>
  <Requires/>
  <Config Name="THREADFIN_CONF" Target="/home/threadfin/conf" Default="" Mode="rw" Description="" Type="Path" Display="always" Required="false" Mask="false">/mnt/user/appdata/threadfin</Config>
  <Config Name="Host Path 2" Target="/home/threadfin/data" Default="" Mode="rw" Description="" Type="Path" Display="always" Required="false" Mask="false">/mnt/user/appdata/threadfin/data</Config>
  <Config Name="Host Path 3" Target="/home/threadfin/conf/backup" Default="" Mode="rw" Description="" Type="Path" Display="always" Required="false" Mask="false">/mnt/user/appdata/threadfin/backup</Config>
  <Config Name="Main Port" Target="34400" Default="34400" Mode="tcp" Description="" Type="Port" Display="always" Required="false" Mask="false">34400</Config>
</Container>


