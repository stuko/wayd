# wayd

mvn -DaltDeploymentRepository=snapshot::default::file:../wayd/snapshots clean deploy

###################################
# wayd boot copy in W2K
###################################
copy /Y ..\wayd-boot\target\*.jar .\

###################################
# wayd library copy in W2K
###################################
mkdir wayd-lib
copy /Y ..\wayd-new-base\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-configmanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-containermanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-gcm\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-systemmanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-enginemanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-lockmanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-threadmanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-monitormanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-profilemanager\target\*.jar .\wayd-lib\
copy /Y ..\wayd-new-3tyenginemanager\target\*.jar .\wayd-lib\

mkdir dependency-lib
copy /Y ..\wayd-new-base\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-configmanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-containermanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-gcm\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-systemmanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-enginemanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-lockmanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-threadmanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-monitormanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-profilemanager\target\lib\*.jar .\dependency-lib\
copy /Y ..\wayd-new-3tyenginemanager\target\lib\*.jar .\dependency-lib\


###################################
# wayd boot copy in W2K
###################################
cp -rf ../wayd-boot/target/*.jar ./

###################################
# wayd library copy in LINUX
###################################
mkdir wayd-lib
cp -rf ../wayd-new-base/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-configmanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-containermanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-gcm/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-systemmanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-enginemanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-lockmanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-threadmanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-monitoringmanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-profilemanager/target/*.jar ./wayd-lib/
cp -rf ../wayd-new-3tyenginemanager/target/*.jar ./wayd-lib/

mkdir dependency-lib
cp -rf ../wayd-new-base/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-configmanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-containermanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-gcm/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-systemmanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-enginemanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-lockmanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-threadmanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-monitoringmanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-profilemanager/target/lib/*.jar ./dependency-lib/
cp -rf ../wayd-new-3tyenginemanager/target/lib/*.jar ./dependency-lib/

