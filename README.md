# archi-nls

Archi — http://www.archimatetool.com.

Generated NLS resources for Archi localization from version 4.0.0 and later

This is useful for matching localization changes from version to version.

When you need to up your local version resources, you may check the difference between english NLS changes and modify your language accordingly.

All generated versions are tagged with version tag name, so when you need to get up-to difference you may use the `git diff ${version}` command to see all the resources difference.

## How to contribute

1. Setup Eclipse IDE according to [Archi instruction](http://www.archimatetool.com/dev/eclipse-setup)
2. Import code according to [Archi instruction](http://www.archimatetool.com/dev/import-code)
3. Clone this repository
4. Execute `git tag` in `${ARCHI-NLS-DIR}` to check the latest Archi version applied and remember it as `${ARCHI-NLS-VERSION}` say `4.2.0`
5. Execute `git tag` in `${ARCHI-DIR}` to check the latest Archi release code available
6. Select the Archi release version next to `${ARCHI-NLS-VERSION}` say `4.2.1` and remember it as `${ARCHI-VERSION}`
7. Checkout the selected Archi tag with command `cd ${ARCHI-DIR} && git checkout release_${ARCHI-VERSION} && git clean -d -f`
8. Generate Archi NLS resources in Eclipse IDE according to [Archi instruction](http://www.archimatetool.com/dev/translate-archi)
9. Delete all `archi-nls` directories with command `rm -rf ${ARCHI-NLS-DIR}/com.*`
10. Copy generated NLS resources to `${ARCHI-NLS-DIR}` with command `cp -r ${ARCHI-DIR}/nls/* ${ARCHI-NLS-DIR}`
11. Commit and tag new `archi-nls` version with command `cd ${ARCHI-NLS-DIR} && git add . && git commit -am "${ARCHI-NLS-VERSION} -> ${ARCHI-VERSION}" && git tag ${ARCHI-VERSION}`
12. Repeat steps 6-11 until ${ARCHI-NLS-VERSION} become the latest Archi release version.


