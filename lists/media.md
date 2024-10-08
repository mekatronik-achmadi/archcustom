# Media Packages

## Official

### install graphic tools

inkscape pstoedit djview
imagemagick gimp xsane-gimp

--------------------------------------------------------------------------------

## AUR

### install web-browser

- https://aur.archlinux.org/packages/google-chrome/

### install markdown tools

- https://aur.archlinux.org/packages/pandoc-bin/

### install screencast tools

- https://aur.archlinux.org/packages/simplescreenrecorder/

### install youtube downloader

- https://aur.archlinux.org/packages/yt-dlp-git/

--------------------------------------------------------------------------------

## External

### install markdown tools

- https://github.com/mekatronik-achmadi/archmate/tree/main/pkgbuilds/optional/ghostwriter-qt5/

--------------------------------------------------------------------------------

## Configurations

### configure youtube-dl

Format recommendations:
- vid code -> https | avc1.4D401F 803k video only 720p
- aud code -> https │ audio only opus 48k

```sh
yt-dlp -F https://www.youtube.com/watch?v=xxxxxxxxxxx
yt-dlp -f <vid>+<aud> --merge-output-format mp4 https://www.youtube.com/watch?v=xxxxxxxxxxx
yt-dlp -f 136+251 --merge-output-format mp4 https://www.youtube.com/watch?v=xxxxxxxxxxx

yt-dlp -f 251 https://www.youtube.com/watch?v=xxxxxxxxxxx
ffmpeg -i videoname.webm -vn -ab 128k -ar 44100 -y videoname.mp3
rm -vf videoname.webm
```

### ffmpeg fasten video

```sh
ffmpeg -i input.mp4 \
-filter_complex "[0:v]setpts=0.5*PTS[v];[0:a]atempo=2[a]" \
-map "[v]" -map "[a]" -c:v libx264 -c:a aac output.mp4
```
