docs
====

API Documentation for Handsontable

To build the documentation:
* Install the npm dependencies by typing:
```sh
npm install
```
* Create a `.env.json` file in the main directory, and fill it with your Github token data as follows:
```json
{
  "GITHUB_TOKEN": "[insert your gihub token here]"
}
```
* Fetch source code of the Handsontable PRO and CE and build the documentation:
```sh
npm run start
```
* If you encounter the
`Warning: ENOENT: no such file or directory, open 'generated/scripts/doc-versions.js' Use --force to continue.`
problem, create a `generated/scripts` directory structure, by typing:
```sh
mkdir -p generated/scripts
```

After the initial documentation setup, you can use the
```sh
npm run build
```
command, to build the documentation without cloning the Handsontable repos.

To preview the documentation run docker-compose:
```sh
docker-compose -f docker/docker-compose.yml up
```
By default the documentation will be available at http://localhost:8085/docs/{your-docs-version}/tutorial-introduction.html.
