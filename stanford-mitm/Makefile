target: mitm

JAVA            = java
JAVAC           = javac

JAVASRCS        = \
			src/mitm/MITMProxyServer.java \
			src/mitm/ConnectionDetails.java \
			src/mitm/CopyStreamRunnable.java \
			src/mitm/HTTPSProxyEngine.java \
			src/mitm/JSSEConstants.java \
			src/mitm/ProxyEngine.java \
			src/mitm/ProxyDataFilter.java \
			src/mitm/MITMPlainSocketFactory.java \
			src/mitm/MITMSSLSocketFactory.java \
			src/mitm/MITMSocketFactory.java \
			src/mitm/StreamThread.java \
			src/mitm/SignCert.java \
			src/mitm/X509CertificateGenerator.java \

JAVAOBJS        = $(JAVASRCS:.java=.class)

JAVACFLAGS	= -classpath ${CLASSPATH}:.:iaik_jce.jar

.SUFFIXES:	.class .java

.java.class: $*.java
	    $(JAVAC) $(JAVACFLAGS) $*.java;

clean:
	    rm -f src/mitm/*\$*.class src/mitm/*.class src/mitm/*~

mitm:    $(JAVAOBJS)
