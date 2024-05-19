# threadfin-unraid
threadfin xml template for unraid
<img src="https://github.com/jjone/threadfin-unraid/blob/main/Snipaste_2024-05-19_11-22-40.png">

nano /boot/config/plugins/dockerMan/templates-user/my-Threadfin.xml

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
  <Config Name="THREADFIN_CONF" Target="/home/threadfin/conf" Default="" Mode="rw" Description="" Type="Path" Display="always" Required="false" Mask="false">/mnt/user/appdata/threadfi>
  <Config Name="Host Path 2" Target="/home/threadfin/data" Default="" Mode="rw" Description="" Type="Path" Display="always" Required="false" Mask="false">/mnt/user/appdata/threadfin/d>
  <Config Name="Host Path 3" Target="/home/threadfin/conf/backup" Default="" Mode="rw" Description="" Type="Path" Display="always" Required="false" Mask="false">/mnt/user/appdata/thre>
  <Config Name="Main Port" Target="34400" Default="34400" Mode="tcp" Description="" Type="Port" Display="always" Required="false" Mask="false">34400</Config>
</Container>


