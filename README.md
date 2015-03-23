CountryInfo
===========

This is the GitHub repository for the CountryInfo.txt and related utility programs. 
CountryInfo.txt is a general purpose file intended to facilitate natural language 
processing of news reports and political texts. It was originally developed to identify 
states for the text filtering system used in the development of the Correlates of War
project dataset MID4, then extended to incorporate CIA World Factbook and WordNet 
information for the development of TABARI dictionaries. File contains about 32,000 lines 
with country names, synonyms and other alternative forms, major city and region names,
and national leaders. It covers about 240 countries and administrative units 
(e.g. American Samoa, Christmas Island, Hong Kong, Greenland). It is internally documented 
and almost but not quite XML.

Files:

CountryInfo.120116.txt: initial version of file

CountryInfo.140728.txt: 
Revision which has TABARI-style date restrictions on countries which became independent 
in the post-1989 period (mostly former Soviet Union and former Yugoslavia) plus some
additional small corrections. 

format.rulers.org.pl: 
This Perl program translates one or more lines from the Rulers.org web site into the 
CountryInfo.txt format. rulers.org is almost but not quite consistent, so this was a
utility used in the original development of the file; it might be useful for updates.

translate.countryinfo.pl: 
This Perl program translates the CountryInfo.120116.txt file in a TABARI-compatible
file CountryInfo.YYMMDD.actors with some duplicate detection. It has not been modified
to work with the date-restricted country codes in 

PITF_to_ISO3166.txt
A Python dictionary that should get you most of the way to translating between 
the Political Instability Task Force  country codes (SFTGCODE) to the ISO-3166-alpha3 
codes used in ICEWS, Phoenix and pretty much everywhere else. This was done for a specific 
project and may not have all of the codes but should have most of them. Easier than reading
the full CountryInfo file if all you need is this translation.
