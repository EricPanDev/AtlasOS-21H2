yeah so its really easy to get this file to work on a "unsupported" version

just edit the .conf file and add your system version without the decimal as a new entry (find it in winver)

eg if you are trying to add support for 21H2, you would go into winver and see that your system uses 19044.3031,

the file before:
```
	<SupportedBuilds>
		<!-- 22H2 -->
		<string>19045</string>
		<!-- 24H2 -->
		<string>26100</string>
	</SupportedBuilds>
```
the file after:
```
	<SupportedBuilds>
		<!-- 22H2 -->
		<string>19045</string>
		<!-- 24H2 -->
		<string>26100</string>
		<!-- 21H2 -->
		<string>19044</string>
	</SupportedBuilds>
```

then you just install 7zip, select all the files and right click, set archive format to 7z, set the zip password to `malte`, then rename the file from example.7z to example.apbx

i guess this doesnt work for actual unsupported builds but atlas actually will run fine on a lot of systems that claim they are unsupported, if this process doesn't work **please dont bother the atlas team about it**
