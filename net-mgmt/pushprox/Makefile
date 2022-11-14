PORTNAME?=		pushprox
PORTVERSION=		0.1.0
DISTVERSIONPREFIX=	v
CATEGORIES=		net-mgmt

MAINTAINER=	freebsd@rheinwolf.de
COMMENT=	Prometheus push proxy

LICENSE=	APACHE20

USES=		go:modules
USE_GITHUB=	yes
USE_RC_SUBR=	pushprox

GH_ACCOUNT=	prometheus-community
GH_PROJECT=	PushProx
GH_TUPLE=	\
		ShowMax:go-fqdn:6f60894d629f:showmax_go_fqdn/vendor/github.com/ShowMax/go-fqdn \
		alecthomas:kingpin:v2.2.6:alecthomas_kingpin/vendor/gopkg.in/alecthomas/kingpin.v2 \
		alecthomas:template:fb15b899a751:alecthomas_template/vendor/github.com/alecthomas/template \
		alecthomas:units:f65c72e2690d:alecthomas_units/vendor/github.com/alecthomas/units \
		beorn7:perks:v1.0.1:beorn7_perks/vendor/github.com/beorn7/perks \
		cespare:xxhash:v2.1.1:cespare_xxhash_v2/vendor/github.com/cespare/xxhash/v2 \
		go-kit:kit:v0.10.0:go_kit_kit/vendor/github.com/go-kit/kit \
		go-logfmt:logfmt:v0.5.0:go_logfmt_logfmt/vendor/github.com/go-logfmt/logfmt \
		golang:protobuf:v1.4.0:golang_protobuf/vendor/github.com/golang/protobuf \
		golang:sys:1957bb5e6d1f:golang_sys/vendor/golang.org/x/sys \
		google:uuid:v1.1.1:google_uuid/vendor/github.com/google/uuid \
		matttproud:golang_protobuf_extensions:v1.0.1:matttproud_golang_protobuf_extensions/vendor/github.com/matttproud/golang_protobuf_extensions \
		pkg:errors:v0.9.1:pkg_errors/vendor/github.com/pkg/errors \
		prometheus:client_golang:v1.6.0:prometheus_client_golang/vendor/github.com/prometheus/client_golang \
		prometheus:client_model:v0.2.0:prometheus_client_model/vendor/github.com/prometheus/client_model \
		prometheus:common:v0.10.0:prometheus_common/vendor/github.com/prometheus/common \
		prometheus:procfs:v0.0.11:prometheus_procfs/vendor/github.com/prometheus/procfs \
		protocolbuffers:protobuf-go:v1.21.0:protocolbuffers_protobuf_go/vendor/google.golang.org/protobuf

GO_TARGET=	./cmd/proxy:pushprox

USERS=		prometheus
GROUPS=		prometheus

PLIST_FILES=	bin/pushprox
PLIST_SUB=	GROUPS=${GROUPS} \
		USERS=${USERS}

.include <bsd.port.mk>
