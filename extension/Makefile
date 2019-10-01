build: fetch
	mkdir -p build
	inkscape --without-gui packages/chrome.svg --export-png build/chrome.png

package: clean build
	zip --recurse-paths package.zip manifest.json background.js build packages

chrome-web-store: build
	mkdir -p build/chrome-web-store
	inkscape --without-gui packages/chrome.svg --export-png build/chrome-web-store/icon.png --export-width 128 --export-height 128
	inkscape --without-gui packages/chrome.svg --export-png build/chrome-web-store/screenshot.png --export-width 1280 --export-height 800

fetch:
	./fetch

clean:
	rm -Rf build packages package.zip

.PHONY: build fetch
