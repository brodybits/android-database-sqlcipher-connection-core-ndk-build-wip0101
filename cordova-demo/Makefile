all:
	echo 'all target not supported' && exit 1

prepare-plugin:
	mkdir -p cordova-sqlite-demo-plugin/dependencies
	cp ../android-database-sqlcipher-connection-core-glue-ndk.jar cordova-sqlite-demo-plugin/dependencies

prepare-app: prepare-plugin
	cordova plugin add ./cordova-sqlite-demo-plugin
	cordova plugin add cordova-sqlite-storage-file

clean:
	rm -rf node_modules package-lock.json platforms plugins
	rm -rf node_modules platforms plugins
	rm -rf cordova-sqlite-demo-plugin/dependencies

distclean: clean
	rm -rf sqlite-amalgamation-*
