This is a lookup table between old and new fields

###################
# FERMI_GBM_ALERT #
###################
NOTICE_DATE:     alert_datetime (gcn/notices/core/Alert.schema)
NOTICE_TYPE:     gcn.notices.fermi.gbm.alert (inherent in kafka topic name)
RECORD_NUM:      record_number (gcn/notices/core/Reported.schema)
TRIGGER_NUM:     id[1] (gcn/notices/core/Event.schema has option of array for name, use second field for trigger number, first field is the burst number)
GRB_DATE/TIME:   trigger_time (core/DateTime.schema)
   New fields for additional legacy values:
       TJD --> TJD (gcn/notices/fermi/gbm/Core.schema)
       DOY --> DOY (gcn/notices/fermi/gbm/Core.schema)
       SOD --> SOD (gcn/notices/fermi/gbm/Core.schema)
TRIGGER_SIGNIF:  rate_snr (gcn/notices/core/Statistics.schema)
TRIGGER_DUR:     rate_duration (gcn/notices/core/Statistics.schema)
E_RANGE: [keV]   rate_energy_range (gcn/notices/core/Statistics.schema)
    New fields for additional legacy values:
       E_RANGE: [chan] --> rate_energy_chan  (gcn/notices/fermi/gbm/Core.schema)
ALGORITHM:       trigger_algorithm (gcn/notices/fermi/gbm/Core.schema)
DETECTORS:       detectors (gcn/notices/fermi/gbm/Core.schema)
LC_URL:          lightcurve_url (gcn/notices/fermi/gbm/Core.schema)
COMMENTS:        additional_info (gcn/notices/core/AdditionalInfo.schema.json)

#####################
# FERMI_GBM_FLT_POS #
#####################
NOTICE_DATE:     alert_datetime (gcn/notices/core/Alert.schema)
NOTICE_TYPE:     gcn.notices.fermi.gbm.pos.flt (inherent in kafka topic name)
RECORD_NUM:      record_number (gcn/notices/core/Reported.schema)
TRIGGER_NUM:     id[1] (gcn/notices/core/Event.schema has option of array for name, use second field for trigger number, first field is the burst number)
GRB_RA:          ra (gcn/notices/core/Localization.schema)
    New fields for additional legacy values:
        ra_current
        ra_1950
GRB_DEC:         dec (gcn/notices/core/Localization.schema)
    New fields for additional legacy values:
        dec_current
        dec_1950
GRB_ERROR:       dec_uncertainty (gcn/notices/core/Localization.schema)
GRB_INTEN:       intensity (gcn/notices/fermi/gbm/Core.schema)
DATA_SIGNIF:     rate_snr (gcn/notices/core/Statistics.schema)
INTEG_TIME:      rate_duration (gcn/notices/core/Statistics.schema)
GRB_DATE/TIME:   trigger_time (core/DateTime.schema)
   New fields for additional legacy values:
       TJD --> TJD (gcn/notices/fermi/gbm/Core.schema)
       DOY --> DOY (gcn/notices/fermi/gbm/Core.schema)
       SOD --> SOD (gcn/notices/fermi/gbm/Core.schema)
GRB_PHI:         instrument_phi (gcn/notices/core/Localization.schema)
GRB_THETA:       instrument_theta (gcn/notices/core/Localization.schema)
DATA_TIME_SCALE: rate_duration (gcn/notices/core/Statistics.schema)
HARD_RATIO:      hardness_ratio (gcn/notices/core/HardnessRatio.schema.json)
LOC_ALGORITHM:   location_algorithm (gcn/notices/fermi/gbm/Core.schema)
MOST_LIKELY:     classification (gcn/notices/core/Statistics.schema) (dict with most and 2nd most likely classifications. Key is class, value is fractional number)
2nd_MOST_LIKELY: classification (gcn/notices/core/Statistics.schema) (dict with most and 2nd most likely classifications. Key is class, value is fractional number)
DETECTORS:       detectors (gcn/notices/fermi/gbm/Core.schema)
SUN_POSTN:       sun_ra, sun_dec (gcn/notices/fermi/gbm/Core.schema)
SUN_DIST:        sun_distance (gcn/notices/fermi/gbm/Core.schema)
    New fields for additional legacy values:
    Sun_angle --> sun_angle (gcn/notices/fermi/gbm/Core.schema) --> do we need this?
MOON_POSTN:      moon_ra, moon_dec (gcn/notices/fermi/gbm/Core.schema)
MOON_DIST:       moon_distance (gcn/notices/fermi/gbm/Core.schema)
MOON_ILLUM:      moon_illumination (gcn/notices/fermi/gbm/Core.schema)
GAL_COORDS:      gal_lon, gal_lat (gcn/notices/fermi/gbm/Core.schema)
ECL_COORDS:      ecl_lon, ecl_lat (gcn/notices/fermi/gbm/Core.schema)
LC_URL:          lightcurve_url (gcn/notices/fermi/gbm/Core.schema)
COMMENTS:        additional_info (gcn/notices/core/AdditionalInfo.schema.json)

#####################
# FERMI_GBM_GND_POS #
#####################
NOTICE_DATE:     alert_datetime (gcn/notices/core/Alert.schema)
NOTICE_TYPE:     gcn.notices.fermi.gbm.pos.flt (inherent in kafka topic name)
RECORD_NUM:      record_number (gcn/notices/core/Reported.schema)
TRIGGER_NUM:     id[1] (gcn/notices/core/Event.schema has option of array for name, use second field for trigger number, first field is the burst number)
GRB_RA:          ra (gcn/notices/core/Localization.schema)
    New fields for additional legacy values:
        ra_current
        ra_1950
GRB_DEC:         dec (gcn/notices/core/Localization.schema)
    New fields for additional legacy values:
        dec_current
        dec_1950
GRB_ERROR:       dec_uncertainty (gcn/notices/core/Localization.schema)
DATA_SIGNIF:     rate_snr (gcn/notices/core/Statistics.schema)
DATA_INTERVAL:   rate_duration (gcn/notices/core/Statistics.schema)
GRB_DATE/TIME:   trigger_time (core/DateTime.schema)
   New fields for additional legacy values:
       TJD --> TJD (gcn/notices/fermi/gbm/Core.schema)
       DOY --> DOY (gcn/notices/fermi/gbm/Core.schema)
       SOD --> SOD (gcn/notices/fermi/gbm/Core.schema)
GRB_PHI:         instrument_phi (gcn/notices/core/Localization.schema)
GRB_THETA:       instrument_theta (gcn/notices/core/Localization.schema)
E_RANGE: [keV]   rate_energy_range (gcn/notices/core/Statistics.schema)
LOC_ALGORITHM:   ground_sw_version (gcn/notices/fermi/gbm/Core.schema)
SUN_POSTN:       sun_ra, sun_dec (gcn/notices/fermi/gbm/Core.schema)
SUN_DIST:        sun_distance (gcn/notices/fermi/gbm/Core.schema)
    New fields for additional legacy values:
    Sun_angle --> sun_angle (gcn/notices/fermi/gbm/Core.schema) --> do we need this?
MOON_POSTN:      moon_ra, moon_dec (gcn/notices/fermi/gbm/Core.schema)
MOON_DIST:       moon_distance (gcn/notices/fermi/gbm/Core.schema)
MOON_ILLUM:      moon_illumination (gcn/notices/fermi/gbm/Core.schema)
GAL_COORDS:       61.42, 69.20 [deg] galactic lon,lat of the burst (or transient)
ECL_COORDS:      197.01, 45.83 [deg] ecliptic lon,lat of the burst (or transient)
GAL_COORDS:      gal_lon, gal_lat (gcn/notices/fermi/gbm/Core.schema)
ECL_COORDS:      ecl_lon, ecl_lat (gcn/notices/fermi/gbm/Core.schema)
LC_URL:          lightcurve_url (gcn/notices/fermi/gbm/Core.schema)
POS_MAP_URL:     position_map_url (gcn/notices/fermi/gbm/Core.schema)
     New field for map included in Kafka alert
     healpix_file (gcn/notices/core/Localization.schema)
COMMENTS:        additional_info (gcn/notices/core/AdditionalInfo.schema.json)

#######################
# FERMI_GBM_SUBTHRESH #
#######################
NOTICE_DATE:     alert_datetime (gcn/notices/core/Alert.schema)
NOTICE_TYPE:     gcn.notices.fermi.gbm.pos.flt (inherent in kafka topic name)
TRIGGER_NUM:     id  [TRANS_NUM, FULL_ID_NUM]
GRB_RA:          ra (gcn/notices/core/Localization.schema)
    New fields for additional legacy values:
        ra_current
        ra_1950
GRB_DEC:         dec (gcn/notices/core/Localization.schema)
    New fields for additional legacy values:
        dec_current
        dec_1950
TRANS_ERROR:     dec_uncertainty (gcn/notices/core/Localization.schema)
    New field:
        statistical: true (gcn/notices/core/Localization.schema)
TRANS_DURATION:  rate_duration (gcn/notices/core/Statistics.schema)
TRANS_DATE/TIME: trigger_time (core/DateTime.schema)
   New fields for additional legacy values:
       TJD --> TJD (gcn/notices/fermi/gbm/Core.schema)
       DOY --> DOY (gcn/notices/fermi/gbm/Core.schema)
       SOD --> SOD (gcn/notices/fermi/gbm/Core.schema)
EARTH_ANGLE:     earth_angle (gcn/notices/fermi/gbm/Core.schema)
SPECTRAL_CLASS:  spectral_class (gcn/notices/fermi/gbm/Core.schema)
TYPE_CLASS:      classificiation {"SHORT": 1.0, "LONG": 0.0} (gcn/notices/core/Statistics.schema)
RELIABILITY:     reliability (gcn/notices/fermi/gbm/Core.schema)
HEALPIX_URL:     healpix_file/healpix_url (gcn/notices/core/Localization.schema)
MAP_URL:         position_map_url (gcn/notices/fermi/gbm/Core.schema)
LC_URL:          lightcurve_url (gcn/notices/fermi/gbm/Core.schema)
SUN_POSTN:       sun_ra, sun_dec (gcn/notices/fermi/gbm/Core.schema)
SUN_DIST:        sun_distance (gcn/notices/fermi/gbm/Core.schema)
    New fields for additional legacy values:
    Sun_angle --> sun_angle (gcn/notices/fermi/gbm/Core.schema) --> do we need this?
MOON_POSTN:      moon_ra, moon_dec (gcn/notices/fermi/gbm/Core.schema)
MOON_DIST:       moon_distance (gcn/notices/fermi/gbm/Core.schema)
MOON_ILLUM:      moon_illumination (gcn/notices/fermi/gbm/Core.schema)
GAL_COORDS:       61.42, 69.20 [deg] galactic lon,lat of the burst (or transient)
ECL_COORDS:      197.01, 45.83 [deg] ecliptic lon,lat of the burst (or transient)
GAL_COORDS:      gal_lon, gal_lat (gcn/notices/fermi/gbm/Core.schema)
ECL_COORDS:      ecl_lon, ecl_lat (gcn/notices/fermi/gbm/Core.schema)
COMMENTS:        additional_info (gcn/notices/core/AdditionalInfo.schema.json)
