# wayd

git clone https://github.com/stuko/wayd.git
git clone https://github.com/stuko/wayd-boot.git
git clone https://github.com/stuko/wayd-new-base.git
git clone https://github.com/stuko/wayd-new-containermanager.git
git clone https://github.com/stuko/wayd-new-threadmanager.git
git clone https://github.com/stuko/wayd-new-systemmanager.git
git clone https://github.com/stuko/wayd-new-profilemanager.git
git clone https://github.com/stuko/wayd-new-monitormanager.git
git clone https://github.com/stuko/wayd-new-lockmanager.git
git clone https://github.com/stuko/wayd-new-gcm.git
git clone https://github.com/stuko/wayd-new-enginemanager.git
git clone https://github.com/stuko/wayd-new-configmanager.git

--> git clone https://github.com/stuko/XXXXXXXXXXXX.git

mvn -DaltDeploymentRepository=snapshot::default::file:../wayd/snapshots clean deploy
or
mvn clean deploy -DrepositoryId=internal.repo
   and
  <distributionManagement>   
    <repository>
      <id>internal.repo</id>
      <name>Project Release</name>
      <url>file://${project.basedir}/../wayd/release</url>
    </repository>
    <snapshotRepository>
      <uniqueVersion>true</uniqueVersion>
      <id>snapshot.repo</id>
      <name>Project Snapshots</name>
      <url>file://${project.basedir}/../wayd/snapshots</url>
    </snapshotRepository>
  </distributionManagement>  

