# Working with Cloud Storage in R

## Option 1: Box Drive (Recommended for most teams)
- Syncs your Box folders to your local machine — works just like a regular folder
- Easy to use with `read_csv()` or other file functions, no special R packages required  
  ```r
  read_csv("Box/YourProject/data/processed/cleaned_data.csv")
  ```
- Best for collaborative projects where everyone uses Box and the same folder structure
- Be mindful of sync status — files must be available offline if running on unstable internet

## Option 2: `boxr` package (for API-based workflows with Box)
- Connects R to Box via API (requires authentication and setup)
- Allows you to upload/download specific files from Box without syncing your entire folder
- Useful if working on a server or cloud-based RStudio environment  
  ```r
  library(boxr)
  box_auth()
  box_read_csv(file_id = "123456789")
  ```

## Option 3: Google Drive with `googledrive` / `googlesheets4`
- Ideal if your team uses Google Drive for data storage or shared spreadsheets
- Authenticate via browser and read/write files directly from your Drive  
  ```r
  library(googledrive)
  drive_download("my_file.csv", path = "data/my_file.csv", overwrite = TRUE)

  library(googlesheets4)
  read_sheet("https://docs.google.com/spreadsheets/d/your_id")
  ```

---

## Tips for All Options
- Avoid editing raw data — keep it read-only and use scripts for cleaning
- Store your R scripts, raw data, outputs, and documentation in organized subfolders
- Use the `{here}` package for more reproducible paths:  
  ```r
  library(here)
  read_csv(here("data", "processed", "cleaned_data.csv"))
  ```

