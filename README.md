# ReMarkable templates PDF

Copy PDF files as template to ReMarkable tablet. 

This script convert PDF files to SVG and PNG and send them to ReMarkable tablet.

> **Be careful, please backup your ReMarkable tablet before using this script.**
> **This script is provided as is, without any warranty, and can break your ReMarkable tablet.**

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

Copy the `.env.example` file and replace values with correct informations.

In order to retrieve password and IP address, on your ReMarkable tablet, go to `Settings > General > About` and click on the `Copyrights and licenses`.

Then run the script:

```bash
./remarkable-templates-pdf.sh
```

You can use the `--dry-run` option to see what will be done. Images and JSON files will be moved to `/tmp/test` directory on the ReMarkable tablet.

## License

MIT. See [LICENSE](./LICENSE) file.