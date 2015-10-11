# Overview
Skeleton is a frame to create your own Go presentations à la
x/tools/cmd/present and optionally host them on App Engine.

Have you seen presentations like Dmitry Vyukov's [Go Dynamic Tools](
http://talks.golang.org/2015/dynamic-tools.slide) and wonder how they
were put together and hosted?  They're pretty nifty, right?  If so,
they are presented using the [x/tools/cmd/present facility](https://godoc.org/golang.org/x/tools/cmd/present).
The presentation media follows an in-house markup that is described in
[package present](https://godoc.org/golang.org/x/tools/present).

## Instructions for Local Presentations

  1. Clone this repository.

  2. Modify and extend `skeleton.slide` to your satisfaction.

  3. Get the present tool: `go get golang.org/x/tools/cmd/present`.

  4. Present away: `present .`.

## Instructions for App Engine-Hosted Presentations

  1. Follow the instructions above to your satisfaction.

  2. Create an account with Google, if necessary.

  3. Acquire the [Go App Engine SDK](https://cloud.google.com/appengine/docs/go/).

  4. Create a new App Engine application on the [Developer Console](https://console.developers.google.com/).

  5. Copy the `x/tools/cmd/present` directory into this directory such that
     it appears as follows:

     ```
     $ ls -l   
     total 40
     -rw-r--r--   1 mtp  eng  11358 Oct 11 11:11 LICENSE
     -rw-r--r--   1 mtp  eng   1320 Oct 11 12:05 README.md
     -rw-r--r--   1 mtp  eng    226 Oct 11 11:11 app.yaml
     drwxr-xr-x  12 mtp  eng    408 Oct 11 12:05 present
     -rw-r--r--   1 mtp  eng      0 Oct 11 12:06 skeleton.slide
     ```

  6. Edit `app.yaml` to your satisfaction.

  7. Test the presentation locally: `goapp serve`.

  8. Deploy to App Engine: `goapp deploy`.

