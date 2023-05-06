# Clipshare

Do you ever have to work on multiple machines?

Do you ever used your Github™ Gists just to send some text between then?

Clipshare is here to save the day!

You can now share your clipboard between your machines (well, given they are on the same network).

## How to use

On one machine:
```bash
$ clipshare
Run `clipshare 11337` on another machine of your network
```

And then on another machine on the same network
```bash
$ clipshare 113377
Connecting to clipboard 113377...
Clipboards connected
```

And voilá, the clipboards of both machines are now magically the same!

## Instalation

### GitHub Releasees (Pre-Built Binaries)
Each release comes with pre-build binaries of several platforms. Grab it from [Github Releases](https://github.com/reu/clipshare/releases).

### Cargo
If you are a Rust enthusiast, installing via Cargo is just:
```bash
$ cargo install clipshare
```

### From source
Make sure you have Rust installed, then:
```bash
$ git clone https://github.com/reu/clipshare.git
$ cd clipshare
$ cargo build --release
$ cp ./target/release/clipshare /usr/local/bin/
```

## Limitations

Yes

<sup><sub>Really, it is quite limited, it can only share utf8 encoded text. Unfortunately you can´t share files for now.</sub></sup>

## Implementation

Nothing fancy here, we just broadcast the internal ip on the network and connect the processes using the informed ~~port~~ "clipboard code".
