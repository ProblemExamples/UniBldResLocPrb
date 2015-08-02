# MyProj - README

This project is just a minimal bug/problem demonstration.

## Problem
How to construct the path to a resource used during the build (specifically the *verify* phase), so it will be found whether maven was executed on the aggregation root or on the child module directly.

## Specific Example
The path to *javaHeaderRegexTemplate.txt* induced into *checkstyle.xml* is correct when running this (**BUILD SUCCESS**):

	cd UniBldResLocPrb/modules/child/
	mvn package

But it is incorrect when running this (**BUILD FAILURE**):

	cd UniBldResLocPrb/
	mvn package

