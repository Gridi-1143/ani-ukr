<h5 align=center>
ani-ukr це програма для перегляду аніме з сайту <a href="https://anitube.in.ua/">Anitube.in.ua</a> в терміналі. Працює на Linux (та можливо MacOS). Натхнення для проєкту взято з <a href="https://github.com/pystardust/ani-cli">ani-cli</a>
</h5>

## Спершу потрібно встановити залежності
- grep
- sed
- curl
- jq
- fzf
- mpv (плеєр)
- iina (плеєр для MacOS)
- yt-dlp (опціонально, для завантаження відео)
- ffmpeg (опціонально, для завантаження відео)
- aria2c (опціонально, для завантаження відео)

### Встановлення залежностей на кожному дистрибутиві відрізняється
<details><summary>Arch</summary>

```sh
sudo pacman -Syy
sudo pacman -S grep sed curl jq fzf mpv yt-dlp ffmpeg aria2
```
</details>

<details><summary>Debian / Ubuntu / Mint</summary>

```sh
sudo apt update
sudo apt install grep sed curl jq fzf mpv yt-dlp ffmpeg aria2
```
</details>

## Встановлення ani-ukr
```sh 
git clone "https://github.com/Gridi-1143/ani-ukr"

sudo chmod +x ani-ukr/ani-ukr

sudo cp ani-ukr/ani-ukr /usr/local/bin
#або 
sudo cp ani-ukr/ani-ukr ~/.local/bin

rm -rf ani-ukr
```
## MacOS 
Я не маю змоги тестувати на MacOS, але по ідеї код має працювати так само, як і на Linux, тому можете спробувати
<details><summary>Встановлення</summary>

Завантажте [HomeBrew](https://docs.brew.sh/Installation)

*Встановити залеженості можете так*

```sh
brew install curl jq grep aria2 ffmpeg git fzf yt-dlp && \
brew install --cask iina
```
І тоді

```sh
git clone "https://github.com/pystardust/ani-cli.git" && cd ./ani-cli
cp ./ani-cli "$(brew --prefix)"/bin
cd .. && rm -rf ./ani-cli
```
</details>

## Видалення
<details><summary>Linux</summary>

```sh 
rm /usr/bin/ani-ukr
#або якщо встановили в іншу директорію
rm ~/.local/bin/ani-ukr
```
</details>
<details><summary>MacOS</summary>

```sh 
rm "$(brew --prefix)/bin/ani-ukr"
```
</details>
