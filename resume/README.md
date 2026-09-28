# Resume folder

The "DOWNLOAD RESUME" and "VIEW PDF" buttons in the RESUME room (and the
`resume` Batcomputer terminal command) all point at one file:

```
resume/Hrithik_Patil_Resume.pdf
```

To update your resume, just replace that file with a new PDF **using the
exact same name** — no code changes needed. If the file is ever missing,
the site fails gracefully with a toast message instead of a broken
download.
