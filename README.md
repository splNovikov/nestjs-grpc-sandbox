# gRPC Tutorial

[NestJS gRPC Microservices Tutorial](https://www.youtube.com/watch?v=UkWcjVWs2UQ&ab_channel=MichaelGuay)

Communication b/w services

**Their Github:**

https://github.com/mguay22/nestjs-grpc

new app:

```tsx
nest new nestjs-grpc-sandbox
```

convert to monorepo:

```tsx
nest generate app auth
```

generate full module in app:

```tsx
nest g resource users
```

install other deps:

```tsx
npm i --save @nestjs/microservices @grpc/grpc-js @grpc/proto-loader ts-proto
```

generate typescript code:

```tsx
protoc --plugin=./node_modules/.bin/protoc-gen-ts_proto --ts_proto_out=./ --ts_proto_opt=nestJs=true ./proto/auth.proto
```

generate a Lib

```tsx
nest g lib common
```

now, start both microservices
```tsx
nest start --watch api-gateway
nest start --watch auth
```