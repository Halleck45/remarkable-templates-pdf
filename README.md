# ReMarkable templates from PDF

Copy PDF files to ReMarkable tablet as templates.

This script will convert PDF files to PNG images and JSON files, then copy them to the ReMarkable tablet via SSH.

> **Be careful, please backup your ReMarkable tablet before using this script.**
> **This script is provided as is, without any warranty, and can break your ReMarkable tablet.**
> I've tested it on my ReMarkable tablet, and it works fine, but I can't guarantee it will work on yours.

## Requirements

Any linux distribution with:

- `bash`
- `convert` (from `imagemagick`)
- `pdf2svg`
- `jq`
- `sshpass`

For example, on Debian derivatives:

```bash
sudo apt install imagemagick pdf2svg jq sshpass
```

## Usage

Place your PDF files in the `templates` directory.

Copy the `.env.example` file to `.env` and edit it to set your ReMarkable tablet IP address and password.

```bash
cp .env.example .env
```

In order to retrieve password and IP address, on your ReMarkable tablet, go to `Settings > General > About` and click on the `Copyrights and licenses`.

Then run the script:

```bash
./remarkable-templates-pdf
```

You can use the `--dry-run` option to see what will be done. Images and JSON files will be moved to `/tmp/test` directory on the ReMarkable tablet.

## License

MIT. See [LICENSE](./LICENSE) file.