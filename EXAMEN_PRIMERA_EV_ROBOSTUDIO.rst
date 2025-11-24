 PROC main()
       PROGRAMA_1;
       
    ENDPROC
    PROC Asignacion()
        MoveL HOME,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveL pick_pieza,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveL place_1,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveL place_2,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveL place_3,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
    ENDPROC
    PROC PROGRAMA_1()

        MoveJ HOME,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveL OFFS (pick_pieza,0,0,200),v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO pick_pieza,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,1;
        MoveL OFFS (pick_pieza,0,0,200),v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        WaitDI pieza,1;
        IF place=1 and back = FALSE 
        THEN 
        MoveL OFFS (place_1,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO place_1,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,0;
        MoveL OFFS (place_1,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        ELSEIF  PLACE=2 AND BACK=FALSE 
        THEN
        MoveL OFFS (place_2,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO place_2,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,0;
        MoveL OFFS (place_2,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        ELSEIF place=3 AND BACK=FALSE
        THEN
        MoveL OFFS (place_3,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO place_3,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,0;
        MoveL OFFS (place_3,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        ELSEIF  PLACE=1 AND BACK=TRUE THEN
        MoveL OFFS (place_1,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO place_1,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,0;
        MoveL OFFS (place_1,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO place_1,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,1;
        MoveL OFFS (place_1,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveL OFFS (pick_pieza,0,0,200),v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO pick_pieza,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,0;
        MoveL OFFS (pick_pieza,0,0,200),v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        ELSEIF  PLACE=2 AND BACK=TRUE 
        THEN
        MoveL OFFS (place_2,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO place_2,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,0;
        MoveL OFFS (place_2,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO place_2,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,1;
        MoveL OFFS (place_2,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveL OFFS (pick_pieza,0,0,200),v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO pick_pieza,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,0;
        MoveL OFFS (pick_pieza,0,0,200),v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        ELSEIF  PLACE=3 AND BACK=TRUE 
        THEN
        MoveL OFFS (place_3,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO place_3,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,0;
        MoveL OFFS (place_3,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO place_3,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,1;
        MoveL OFFS (place_3,0,0,200), v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveL OFFS (pick_pieza,0,0,200),v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        MoveLDO pick_pieza,v200,z0,TCP_Ventosa\WObj:=Caja_Piezas,vacio,0;
        MoveL OFFS (pick_pieza,0,0,200),v200,z0,TCP_Ventosa\WObj:=Caja_Piezas;
        ENDIF

    ENDPROC
ENDMODULE