#' Import Zip Files
#'
#' Take a URL for a zip folder and import into Posit Workbench. It will create the location folder if not specified,
#' otherwise will just save to the folder
#' @param {zip_file} {A complete URL to the web-based zip folder that ends in .zip}
#' @param {location} {Specify the directory you want to install into.}
import_zip <- function(zip_file, location) {

  if(!endsWith(zip_file, ".zip")) {
    return("Not a zip folder. Please check the file location")
  }

  if(!file.exists(location)) {

    if(!endsWith(location, "/")) { #if doesn't end with a slash, add one
      location <- paste0(location, "/")
    }

    dir.create(location)

  }

    name <- paste0(location, "temp")


  if(endsWith(zip_file, ".zip")) {
  download.file(zip_file, destfile = name) #download the zip
  unzip(name, exdir = location) #unpack the zip folder, into the directory
  unlink(name) #remove the temp folder
  }

  }
