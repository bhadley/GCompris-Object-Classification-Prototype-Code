
SUBDIRS = \
	australia \
	argentina \
	brazil \
	canada \
	china \
	france \
	germany \
	italy  \
	india \
	mexico \
	norway \
	poland \
	turkey \
	usa

xmldir = $(pkgdatadir)/@PACKAGE_DATA_DIR@/classify_objects

xml_in_files = \
	board1_0.xml.in \
	board2_0.xml.in \
	board3_0.xml.in \
	board4_0.xml.in \
	board5_0.xml.in \
	board5_1.xml.in \
	board5_2.xml.in \
	board6_0.xml.in \
	board7_0.xml.in \
	board8_0.xml.in \
	board9_0.xml.in \
	board10_0.xml.in \
	board10_1.xml.in \
	board11_0.xml.in \
	board11_1.xml.in \
	board11_2.xml.in \
	board11_3.xml.in \
	board12_0.xml.in \
	board13_0.xml.in  \
	board14_0.xml.in 

xml_DATA = $(xml_in_files:.xml.in=.xml)

#
# Do not use the INTLTOOL_XML_RULE, we don't need to embed the translations
# in the file themselves. GCompris pick the translations from the po file at
# runtime.
#
$(xml_DATA): %.xml: %.xml.in
	sed -e "s/\(<\{1\}\/*\)_/\1/g" $< > $@

CLEANFILES = $(xml_DATA)
EXTRA_DIST = ${xml_in_files}
