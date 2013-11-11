Gps Coordinates Parser
====================

Simple GPS coordinates parsing library for Java language.


Example unittest:

        geo.gps.Coordinates gps = new geo.gps.Coordinates();
        geo.gps.Coordinates gpsTB = new geo.gps.Coordinates(48.16, 17.13); // Bratislava
        
        // Bratislava
        assertTrue(gps.parse("48 9 36, 17 7 48"));
        assertTrue(gps.equals(gpsTB));
        
        assertTrue(gps.parse("N48 9 36, E17 7 48"));
        assertTrue(gps.equals(gpsTB));
        
        assertTrue(gps.parse("+48 9 36, +17 7 48"));
        assertTrue(gps.equals(gpsTB));
        
        assertTrue(gps.parse("48 9 36N, 17 7 48E"));        
        assertTrue(gps.equals(gpsTB));
        
        assertTrue(gps.parse("48 9 36 17 7 48"));        
        assertTrue(gps.equals(gpsTB));
        
        assertTrue(gps.parse("N48 9 36 E17 7 48"));
        assertTrue(gps.equals(gpsTB));
        
        assertTrue(gps.parse("48 9 36N 17 7 48E"));                        
        assertTrue(gps.equals(gpsTB));