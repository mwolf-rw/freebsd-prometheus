PORTNAME=		postgres_exporter
PORTVERSION=		0.11.1
DISTVERSIONPREFIX=	v
CATEGORIES=		databases

MAINTAINER=	freebsd@rheinwolf.de
COMMENT=	Prometheus metrics exporter for PostgreSQL

LICENSE=	APACHE20

USES=		go:modules
USE_GITHUB=	yes
USE_RC_SUBR=	postgres_exporter

GH_ACCOUNT=	prometheus-community
GH_TUPLE=	\
		alecthomas:kingpin:v2.2.6:alecthomas_kingpin/vendor/gopkg.in/alecthomas/kingpin.v2 \
		alecthomas:template:fb15b899a751:alecthomas_template/vendor/github.com/alecthomas/template \
		alecthomas:units:f65c72e2690d:alecthomas_units/vendor/github.com/alecthomas/units \
		beorn7:perks:v1.0.1:beorn7_perks/vendor/github.com/beorn7/perks \
		blang:semver:v3.5.1:blang_semver/vendor/github.com/blang/semver \
		cespare:xxhash:v2.1.2:cespare_xxhash_v2/vendor/github.com/cespare/xxhash/v2 \
		go-check:check:10cb98267c6c:go_check_check/vendor/gopkg.in/check.v1 \
		go-kit:log:v0.2.1:go_kit_log/vendor/github.com/go-kit/log \
		go-logfmt:logfmt:v0.5.1:go_logfmt_logfmt/vendor/github.com/go-logfmt/logfmt \
		go-yaml:yaml:v2.4.0:go_yaml_yaml/vendor/gopkg.in/yaml.v2 \
		golang:appengine:v1.6.6:golang_appengine/vendor/google.golang.org/appengine \
		golang:crypto:5ff15b29337e:golang_crypto/vendor/golang.org/x/crypto \
		golang:net:27dd8689420f:golang_net/vendor/golang.org/x/net \
		golang:oauth2:ee480838109b:golang_oauth2/vendor/golang.org/x/oauth2 \
		golang:protobuf:v1.5.2:golang_protobuf/vendor/github.com/golang/protobuf \
		golang:sys:da31bd327af9:golang_sys/vendor/golang.org/x/sys \
		golang:text:v0.3.7:golang_text/vendor/golang.org/x/text \
		jpillora:backoff:v1.0.0:jpillora_backoff/vendor/github.com/jpillora/backoff \
		kr:pretty:v0.2.1:kr_pretty/vendor/github.com/kr/pretty \
		kr:text:v0.1.0:kr_text/vendor/github.com/kr/text \
		lib:pq:v1.10.6:lib_pq/vendor/github.com/lib/pq \
		matttproud:golang_protobuf_extensions:v1.0.1:matttproud_golang_protobuf_extensions/vendor/github.com/matttproud/golang_protobuf_extensions \
		mwitkow:go-conntrack:2f068394615f:mwitkow_go_conntrack/vendor/github.com/mwitkow/go-conntrack \
		pkg:errors:v0.9.1:pkg_errors/vendor/github.com/pkg/errors \
		prometheus:client_golang:v1.12.2:prometheus_client_golang/vendor/github.com/prometheus/client_golang \
		prometheus:client_model:v0.2.0:prometheus_client_model/vendor/github.com/prometheus/client_model \
		prometheus:common:v0.35.0:prometheus_common/vendor/github.com/prometheus/common \
		prometheus:exporter-toolkit:v0.7.1:prometheus_exporter_toolkit/vendor/github.com/prometheus/exporter-toolkit \
		prometheus:procfs:v0.7.3:prometheus_procfs/vendor/github.com/prometheus/procfs \
		protocolbuffers:protobuf-go:v1.26.0:protocolbuffers_protobuf_go/vendor/google.golang.org/protobuf

GO_TARGET=	./cmd/postgres_exporter:${PORTNAME}

USERS=		postgres
GROUPS=		postgres

PLIST_FILES=	bin/postgres_exporter
PLIST_SUB=	GROUPS=${GROUPS} \
		USERS=${USERS}

.include <bsd.port.mk>
