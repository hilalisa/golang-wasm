FROM nlepage/golang_wasm AS builder

COPY ./ src/hello/
RUN go build -o test.wasm hello

FROM nlepage/golang_wasm:nginx

COPY --from=builder /go/test.wasm /usr/share/nginx/html/
